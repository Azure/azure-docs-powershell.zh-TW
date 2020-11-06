---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: e10e60845c9aeb90b7c708a65f7d681d9894b022
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613318"
---
# <span data-ttu-id="90e28-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="90e28-101">New-AzHost</span></span>

## <span data-ttu-id="90e28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90e28-102">SYNOPSIS</span></span>
<span data-ttu-id="90e28-103">建立主機。</span><span class="sxs-lookup"><span data-stu-id="90e28-103">Creates a  host.</span></span>

## <span data-ttu-id="90e28-104">句法</span><span class="sxs-lookup"><span data-stu-id="90e28-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e28-105">說明</span><span class="sxs-lookup"><span data-stu-id="90e28-105">DESCRIPTION</span></span>
<span data-ttu-id="90e28-106">這個 Cmdlet 會建立主機。</span><span class="sxs-lookup"><span data-stu-id="90e28-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="90e28-107">示例</span><span class="sxs-lookup"><span data-stu-id="90e28-107">EXAMPLES</span></span>

### <span data-ttu-id="90e28-108">範例1</span><span class="sxs-lookup"><span data-stu-id="90e28-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="90e28-109">這個命令會在指定的主機群組和指定的位置中建立給定 Sku 的主機。</span><span class="sxs-lookup"><span data-stu-id="90e28-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="90e28-110">參數</span><span class="sxs-lookup"><span data-stu-id="90e28-110">PARAMETERS</span></span>

### <span data-ttu-id="90e28-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90e28-111">-AsJob</span></span>
<span data-ttu-id="90e28-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="90e28-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90e28-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="90e28-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="90e28-114">指定是否應在失敗時自動取代主機。</span><span class="sxs-lookup"><span data-stu-id="90e28-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="90e28-115">未提供時，該值預設為 [true]。</span><span class="sxs-lookup"><span data-stu-id="90e28-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e28-116">-DefaultProfile</span></span>
<span data-ttu-id="90e28-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90e28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="90e28-118">-HostGroupName</span></span>
<span data-ttu-id="90e28-119">指定主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e28-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="90e28-120">-LicenseType</span></span>
<span data-ttu-id="90e28-121">指定將套用至主機上部署之 Vm 的軟體授權類型。</span><span class="sxs-lookup"><span data-stu-id="90e28-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="90e28-122">可能的值為： None、Windows_Server_Hybrid 和 Windows_Server_Perpetual。</span><span class="sxs-lookup"><span data-stu-id="90e28-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="90e28-123">預設值為 [無]。</span><span class="sxs-lookup"><span data-stu-id="90e28-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-124">-位置</span><span class="sxs-lookup"><span data-stu-id="90e28-124">-Location</span></span>
<span data-ttu-id="90e28-125">指定位置。</span><span class="sxs-lookup"><span data-stu-id="90e28-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="90e28-126">-Name</span></span>
<span data-ttu-id="90e28-127">指定主機的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e28-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="90e28-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="90e28-129">指定主機的平臺容錯網域數目。</span><span class="sxs-lookup"><span data-stu-id="90e28-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="90e28-130">然後，[最小值] 為0，最大值為2。</span><span class="sxs-lookup"><span data-stu-id="90e28-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e28-131">-ResourceGroupName</span></span>
<span data-ttu-id="90e28-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e28-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e28-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="90e28-133">-Sku</span></span>
<span data-ttu-id="90e28-134">指定 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e28-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="90e28-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="90e28-135">-Tag</span></span>
<span data-ttu-id="90e28-136">指定標記。</span><span class="sxs-lookup"><span data-stu-id="90e28-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="90e28-137">-確認</span><span class="sxs-lookup"><span data-stu-id="90e28-137">-Confirm</span></span>
<span data-ttu-id="90e28-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90e28-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e28-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e28-139">-WhatIf</span></span>
<span data-ttu-id="90e28-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90e28-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e28-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90e28-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e28-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e28-142">CommonParameters</span></span>
<span data-ttu-id="90e28-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90e28-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e28-144">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90e28-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e28-145">輸入</span><span class="sxs-lookup"><span data-stu-id="90e28-145">INPUTS</span></span>

### <span data-ttu-id="90e28-146">System.object</span><span class="sxs-lookup"><span data-stu-id="90e28-146">System.String</span></span>

## <span data-ttu-id="90e28-147">輸出</span><span class="sxs-lookup"><span data-stu-id="90e28-147">OUTPUTS</span></span>

### <span data-ttu-id="90e28-148">PSHost 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="90e28-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="90e28-149">筆記</span><span class="sxs-lookup"><span data-stu-id="90e28-149">NOTES</span></span>

## <span data-ttu-id="90e28-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="90e28-150">RELATED LINKS</span></span>