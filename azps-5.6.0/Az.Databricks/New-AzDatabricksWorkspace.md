---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: c49056da040e7259c1cbc0964335f157e00cbecd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904482"
---
# <span data-ttu-id="c49cd-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="c49cd-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="c49cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c49cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c49cd-103">建立新工作區。</span><span class="sxs-lookup"><span data-stu-id="c49cd-103">Creates a new workspace.</span></span>

## <span data-ttu-id="c49cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="c49cd-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c49cd-105">描述</span><span class="sxs-lookup"><span data-stu-id="c49cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c49cd-106">建立新工作區。</span><span class="sxs-lookup"><span data-stu-id="c49cd-106">Creates a new workspace.</span></span>

## <span data-ttu-id="c49cd-107">例子</span><span class="sxs-lookup"><span data-stu-id="c49cd-107">EXAMPLES</span></span>

### <span data-ttu-id="c49cd-108">範例 1：建立 Datab一s workspace</span><span class="sxs-lookup"><span data-stu-id="c49cd-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="c49cd-109">此命令會建立 Datab一s 工作區。</span><span class="sxs-lookup"><span data-stu-id="c49cd-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="c49cd-110">範例 2：使用自訂的虛擬網路建立 Datab一s 工作區</span><span class="sxs-lookup"><span data-stu-id="c49cd-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="c49cd-111">此命令會建立一個 Datab一s 工作區，在資源群組中具有自訂的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c49cd-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="c49cd-112">範例 3：使用啟用加密來建立 Datab一s 工作區</span><span class="sxs-lookup"><span data-stu-id="c49cd-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="c49cd-113">此命令會建立 Datab workspace，並設定它以準備加密。</span><span class="sxs-lookup"><span data-stu-id="c49cd-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="c49cd-114">如需加密的更多設定，請參閱Update-AzDatabricksWorkspace範例。</span><span class="sxs-lookup"><span data-stu-id="c49cd-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="c49cd-115">參數</span><span class="sxs-lookup"><span data-stu-id="c49cd-115">PARAMETERS</span></span>

### <span data-ttu-id="c49cd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c49cd-116">-AsJob</span></span>
<span data-ttu-id="c49cd-117">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c49cd-117">Run the command as a job</span></span>

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

### <span data-ttu-id="c49cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49cd-118">-DefaultProfile</span></span>
<span data-ttu-id="c49cd-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c49cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c49cd-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="c49cd-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="c49cd-121">此欄位應該使用的值。</span><span class="sxs-lookup"><span data-stu-id="c49cd-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="c49cd-122">-位置</span><span class="sxs-lookup"><span data-stu-id="c49cd-122">-Location</span></span>
<span data-ttu-id="c49cd-123">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="c49cd-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="c49cd-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49cd-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="c49cd-125">受管理的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c49cd-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="c49cd-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="c49cd-126">-Name</span></span>
<span data-ttu-id="c49cd-127">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c49cd-127">The name of the workspace.</span></span>

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

### <span data-ttu-id="c49cd-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c49cd-128">-NoWait</span></span>
<span data-ttu-id="c49cd-129">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c49cd-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c49cd-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="c49cd-130">-PrepareEncryption</span></span>
<span data-ttu-id="c49cd-131">準備工作區進行加密。</span><span class="sxs-lookup"><span data-stu-id="c49cd-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="c49cd-132">啟用受管理儲存帳戶的受管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="c49cd-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="c49cd-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="c49cd-133">-PrivateSubnetName</span></span>
<span data-ttu-id="c49cd-134">虛擬網路中私人子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="c49cd-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="c49cd-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c49cd-135">-PublicSubnetName</span></span>
<span data-ttu-id="c49cd-136">虛擬網路中公用子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="c49cd-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="c49cd-137">-RequireInfracryptEncryption</span><span class="sxs-lookup"><span data-stu-id="c49cd-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="c49cd-138">這是一個布林值，指出 DBFS 根檔案系統是否將啟用次要加密層，並包含平臺管理的資料靜態金鑰。</span><span class="sxs-lookup"><span data-stu-id="c49cd-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="c49cd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49cd-139">-ResourceGroupName</span></span>
<span data-ttu-id="c49cd-140">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c49cd-140">The name of the resource group.</span></span>
<span data-ttu-id="c49cd-141">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c49cd-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c49cd-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="c49cd-142">-Sku</span></span>
<span data-ttu-id="c49cd-143">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="c49cd-143">The SKU name.</span></span>

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

### <span data-ttu-id="c49cd-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c49cd-144">-SubscriptionId</span></span>
<span data-ttu-id="c49cd-145">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c49cd-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c49cd-146">-標記</span><span class="sxs-lookup"><span data-stu-id="c49cd-146">-Tag</span></span>
<span data-ttu-id="c49cd-147">資源標記。</span><span class="sxs-lookup"><span data-stu-id="c49cd-147">Resource tags.</span></span>

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

### <span data-ttu-id="c49cd-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c49cd-148">-VirtualNetworkId</span></span>
<span data-ttu-id="c49cd-149">應建立此 Datab一s Cluster 的虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c49cd-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="c49cd-150">-確認</span><span class="sxs-lookup"><span data-stu-id="c49cd-150">-Confirm</span></span>
<span data-ttu-id="c49cd-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c49cd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c49cd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c49cd-152">-WhatIf</span></span>
<span data-ttu-id="c49cd-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c49cd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c49cd-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c49cd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c49cd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49cd-155">CommonParameters</span></span>
<span data-ttu-id="c49cd-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c49cd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49cd-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c49cd-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49cd-158">輸入</span><span class="sxs-lookup"><span data-stu-id="c49cd-158">INPUTS</span></span>

## <span data-ttu-id="c49cd-159">輸出</span><span class="sxs-lookup"><span data-stu-id="c49cd-159">OUTPUTS</span></span>

### <span data-ttu-id="c49cd-160">Microsoft.Azure.PowerShell.Cmdlets.Databworks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c49cd-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="c49cd-161">筆記</span><span class="sxs-lookup"><span data-stu-id="c49cd-161">NOTES</span></span>

<span data-ttu-id="c49cd-162">別名</span><span class="sxs-lookup"><span data-stu-id="c49cd-162">ALIASES</span></span>

## <span data-ttu-id="c49cd-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="c49cd-163">RELATED LINKS</span></span>

