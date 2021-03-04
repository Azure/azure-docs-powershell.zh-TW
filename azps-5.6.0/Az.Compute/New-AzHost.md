---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: adeee59745aa3f14fe3b5580139b17412e496f0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903842"
---
# <span data-ttu-id="723ad-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="723ad-101">New-AzHost</span></span>

## <span data-ttu-id="723ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="723ad-102">SYNOPSIS</span></span>
<span data-ttu-id="723ad-103">建立主機。</span><span class="sxs-lookup"><span data-stu-id="723ad-103">Creates a  host.</span></span>

## <span data-ttu-id="723ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="723ad-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="723ad-105">DESCRIPTION</span></span>
<span data-ttu-id="723ad-106">此 Cmdlet 會建立主機。</span><span class="sxs-lookup"><span data-stu-id="723ad-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="723ad-107">例子</span><span class="sxs-lookup"><span data-stu-id="723ad-107">EXAMPLES</span></span>

### <span data-ttu-id="723ad-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="723ad-108">Example 1</span></span>
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

<span data-ttu-id="723ad-109">此命令會建立指定主機群組和指定位置中指定 SKU 的主機。</span><span class="sxs-lookup"><span data-stu-id="723ad-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="723ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="723ad-110">PARAMETERS</span></span>

### <span data-ttu-id="723ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="723ad-111">-AsJob</span></span>
<span data-ttu-id="723ad-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="723ad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="723ad-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="723ad-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="723ad-114">指定是否應該在失敗時自動取代主機。</span><span class="sxs-lookup"><span data-stu-id="723ad-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="723ad-115">未提供值時，值預設為 "true"。</span><span class="sxs-lookup"><span data-stu-id="723ad-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="723ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723ad-116">-DefaultProfile</span></span>
<span data-ttu-id="723ad-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="723ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="723ad-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="723ad-118">-HostGroupName</span></span>
<span data-ttu-id="723ad-119">指定主機組的名稱。</span><span class="sxs-lookup"><span data-stu-id="723ad-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="723ad-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="723ad-120">-LicenseType</span></span>
<span data-ttu-id="723ad-121">指定將適用于部署在主機上的虛擬機器的軟體授權類型。</span><span class="sxs-lookup"><span data-stu-id="723ad-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="723ad-122">可能的值為：無、Windows_Server_Hybrid及Windows_Server_Perpetual。</span><span class="sxs-lookup"><span data-stu-id="723ad-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="723ad-123">預設值為 None。</span><span class="sxs-lookup"><span data-stu-id="723ad-123">Default value is None.</span></span>

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

### <span data-ttu-id="723ad-124">-位置</span><span class="sxs-lookup"><span data-stu-id="723ad-124">-Location</span></span>
<span data-ttu-id="723ad-125">指定位置。</span><span class="sxs-lookup"><span data-stu-id="723ad-125">Specifies the location.</span></span>

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

### <span data-ttu-id="723ad-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="723ad-126">-Name</span></span>
<span data-ttu-id="723ad-127">指定主機名稱。</span><span class="sxs-lookup"><span data-stu-id="723ad-127">Specifies the name of the host.</span></span>

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

### <span data-ttu-id="723ad-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="723ad-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="723ad-129">指定主機的平臺故障網域數目。</span><span class="sxs-lookup"><span data-stu-id="723ad-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="723ad-130">然後最小值為 0，最大值為 2。</span><span class="sxs-lookup"><span data-stu-id="723ad-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="723ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="723ad-132">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="723ad-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="723ad-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="723ad-133">-Sku</span></span>
<span data-ttu-id="723ad-134">指定 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="723ad-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="723ad-135">-標記</span><span class="sxs-lookup"><span data-stu-id="723ad-135">-Tag</span></span>
<span data-ttu-id="723ad-136">指定標記。</span><span class="sxs-lookup"><span data-stu-id="723ad-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="723ad-137">-確認</span><span class="sxs-lookup"><span data-stu-id="723ad-137">-Confirm</span></span>
<span data-ttu-id="723ad-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="723ad-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="723ad-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723ad-139">-WhatIf</span></span>
<span data-ttu-id="723ad-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="723ad-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="723ad-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="723ad-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="723ad-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723ad-142">CommonParameters</span></span>
<span data-ttu-id="723ad-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="723ad-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723ad-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="723ad-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723ad-145">輸入</span><span class="sxs-lookup"><span data-stu-id="723ad-145">INPUTS</span></span>

### <span data-ttu-id="723ad-146">System.String</span><span class="sxs-lookup"><span data-stu-id="723ad-146">System.String</span></span>

## <span data-ttu-id="723ad-147">輸出</span><span class="sxs-lookup"><span data-stu-id="723ad-147">OUTPUTS</span></span>

### <span data-ttu-id="723ad-148">Microsoft.Azure.Commands.Compute.Automation.models.PSHost</span><span class="sxs-lookup"><span data-stu-id="723ad-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="723ad-149">筆記</span><span class="sxs-lookup"><span data-stu-id="723ad-149">NOTES</span></span>

## <span data-ttu-id="723ad-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="723ad-150">RELATED LINKS</span></span>
