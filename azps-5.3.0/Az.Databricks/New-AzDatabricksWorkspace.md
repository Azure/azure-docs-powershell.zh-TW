---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447919"
---
# <span data-ttu-id="22d0e-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="22d0e-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="22d0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="22d0e-103">建立新的工作區。</span><span class="sxs-lookup"><span data-stu-id="22d0e-103">Creates a new workspace.</span></span>

## <span data-ttu-id="22d0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="22d0e-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22d0e-105">說明</span><span class="sxs-lookup"><span data-stu-id="22d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="22d0e-106">建立新的工作區。</span><span class="sxs-lookup"><span data-stu-id="22d0e-106">Creates a new workspace.</span></span>

## <span data-ttu-id="22d0e-107">示例</span><span class="sxs-lookup"><span data-stu-id="22d0e-107">EXAMPLES</span></span>

### <span data-ttu-id="22d0e-108">範例1：建立 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="22d0e-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="22d0e-109">這個命令會建立 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="22d0e-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="22d0e-110">範例2：建立含自訂虛擬網路的 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="22d0e-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="22d0e-111">這個命令會建立一個含有資源群組中自訂虛擬網路的 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="22d0e-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="22d0e-112">範例3：使用 [啟用加密] 建立 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="22d0e-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="22d0e-113">這個命令會建立 Databricks 工作區，並將它設定為準備加密。</span><span class="sxs-lookup"><span data-stu-id="22d0e-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="22d0e-114">如需加密的其他設定，請參閱 Update-AzDatabricksWorkspace 的範例。</span><span class="sxs-lookup"><span data-stu-id="22d0e-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="22d0e-115">參數</span><span class="sxs-lookup"><span data-stu-id="22d0e-115">PARAMETERS</span></span>

### <span data-ttu-id="22d0e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22d0e-116">-AsJob</span></span>
<span data-ttu-id="22d0e-117">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="22d0e-117">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d0e-118">-DefaultProfile</span></span>
<span data-ttu-id="22d0e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-120">-位置</span><span class="sxs-lookup"><span data-stu-id="22d0e-120">-Location</span></span>
<span data-ttu-id="22d0e-121">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="22d0e-121">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d0e-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="22d0e-123">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="22d0e-124">-Name</span></span>
<span data-ttu-id="22d0e-125">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-125">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="22d0e-126">-NoWait</span></span>
<span data-ttu-id="22d0e-127">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="22d0e-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="22d0e-128">-PrepareEncryption</span></span>
<span data-ttu-id="22d0e-129">準備工作區以進行加密。</span><span class="sxs-lookup"><span data-stu-id="22d0e-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="22d0e-130">啟用受管理的儲存空間帳戶的 Managed 身分識別。</span><span class="sxs-lookup"><span data-stu-id="22d0e-130">Enables the Managed Identity for managed storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="22d0e-131">-PrivateSubnetName</span></span>
<span data-ttu-id="22d0e-132">虛擬網路內專用子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-132">The name of the Private Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="22d0e-133">-PublicSubnetName</span></span>
<span data-ttu-id="22d0e-134">虛擬網路中公用子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-134">The name of a Public Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="22d0e-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="22d0e-136">布林值，指出 DBFS 根檔案系統是否會啟用次要加密的輔助圖層，以及使用平臺管理金鑰存放在 rest 上的資料。</span><span class="sxs-lookup"><span data-stu-id="22d0e-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d0e-137">-ResourceGroupName</span></span>
<span data-ttu-id="22d0e-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-138">The name of the resource group.</span></span>
<span data-ttu-id="22d0e-139">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="22d0e-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="22d0e-140">-Sku</span></span>
<span data-ttu-id="22d0e-141">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="22d0e-141">The SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22d0e-142">-SubscriptionId</span></span>
<span data-ttu-id="22d0e-143">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="22d0e-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="22d0e-144">-Tag</span></span>
<span data-ttu-id="22d0e-145">資源標記。</span><span class="sxs-lookup"><span data-stu-id="22d0e-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="22d0e-146">-VirtualNetworkId</span></span>
<span data-ttu-id="22d0e-147">要在其中建立此 Databricks 群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="22d0e-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-148">-確認</span><span class="sxs-lookup"><span data-stu-id="22d0e-148">-Confirm</span></span>
<span data-ttu-id="22d0e-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22d0e-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d0e-150">-WhatIf</span></span>
<span data-ttu-id="22d0e-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22d0e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d0e-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22d0e-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d0e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d0e-153">CommonParameters</span></span>
<span data-ttu-id="22d0e-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22d0e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d0e-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22d0e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d0e-156">輸入</span><span class="sxs-lookup"><span data-stu-id="22d0e-156">INPUTS</span></span>

## <span data-ttu-id="22d0e-157">輸出</span><span class="sxs-lookup"><span data-stu-id="22d0e-157">OUTPUTS</span></span>

### <span data-ttu-id="22d0e-158">IWorkspace （Databricks）。 Api20180401。</span><span class="sxs-lookup"><span data-stu-id="22d0e-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="22d0e-159">筆記</span><span class="sxs-lookup"><span data-stu-id="22d0e-159">NOTES</span></span>

<span data-ttu-id="22d0e-160">別名</span><span class="sxs-lookup"><span data-stu-id="22d0e-160">ALIASES</span></span>

## <span data-ttu-id="22d0e-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="22d0e-161">RELATED LINKS</span></span>

