---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: 0d7efa268709d0691fe55bfaf322bd9accf79dab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913657"
---
# <span data-ttu-id="8887e-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="8887e-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="8887e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8887e-102">SYNOPSIS</span></span>
<span data-ttu-id="8887e-103">設定 Azure SQL 實例集區的屬性。</span><span class="sxs-lookup"><span data-stu-id="8887e-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8887e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8887e-104">SYNTAX</span></span>

### <span data-ttu-id="8887e-105">DefaultSetInstancePoolParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8887e-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8887e-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="8887e-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8887e-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="8887e-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8887e-108">描述</span><span class="sxs-lookup"><span data-stu-id="8887e-108">DESCRIPTION</span></span>
<span data-ttu-id="8887e-109">**Set-AzSqlInstancePool** Cmdlet 會修改 Azure SQL 實例集區的屬性。</span><span class="sxs-lookup"><span data-stu-id="8887e-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8887e-110">例子</span><span class="sxs-lookup"><span data-stu-id="8887e-110">EXAMPLES</span></span>

### <span data-ttu-id="8887e-111">範例 1：設定實例集區授權類型</span><span class="sxs-lookup"><span data-stu-id="8887e-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="8887e-112">此命令會設定名稱為 instancePool0 的實例集區之授權類型和/或標籤。</span><span class="sxs-lookup"><span data-stu-id="8887e-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="8887e-113">範例 2：使用實例集區物件設定實例集區授權類型</span><span class="sxs-lookup"><span data-stu-id="8887e-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="8887e-114">此命令會使用實例集區物件來設定實例集區授權類型和/或標記。</span><span class="sxs-lookup"><span data-stu-id="8887e-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="8887e-115">範例 3：使用實例資料庫資源識別碼設定實例集區授權類型</span><span class="sxs-lookup"><span data-stu-id="8887e-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="8887e-116">此命令會設定名稱為 instancePool0 的實例集區之授權類型和/或標籤。</span><span class="sxs-lookup"><span data-stu-id="8887e-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="8887e-117">參數</span><span class="sxs-lookup"><span data-stu-id="8887e-117">PARAMETERS</span></span>

### <span data-ttu-id="8887e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8887e-118">-AsJob</span></span>
<span data-ttu-id="8887e-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8887e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8887e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8887e-120">-DefaultProfile</span></span>
<span data-ttu-id="8887e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8887e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8887e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8887e-122">-InputObject</span></span>
<span data-ttu-id="8887e-123">實例資料庫輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8887e-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8887e-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8887e-124">-LicenseType</span></span>
<span data-ttu-id="8887e-125">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="8887e-125">Determines which License Type to use.</span></span>
<span data-ttu-id="8887e-126">可能的值為 BASEPrice (具有AHB 折扣) 且 LicenseIncluded (不含AHB 折扣) 。</span><span class="sxs-lookup"><span data-stu-id="8887e-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="8887e-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="8887e-127">-Name</span></span>
<span data-ttu-id="8887e-128">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8887e-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8887e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8887e-129">-ResourceGroupName</span></span>
<span data-ttu-id="8887e-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8887e-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8887e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8887e-131">-ResourceId</span></span>
<span data-ttu-id="8887e-132">實例資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8887e-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8887e-133">-標記</span><span class="sxs-lookup"><span data-stu-id="8887e-133">-Tag</span></span>
<span data-ttu-id="8887e-134">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="8887e-134">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8887e-135">-確認</span><span class="sxs-lookup"><span data-stu-id="8887e-135">-Confirm</span></span>
<span data-ttu-id="8887e-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8887e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8887e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8887e-137">-WhatIf</span></span>
<span data-ttu-id="8887e-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8887e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8887e-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8887e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8887e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8887e-140">CommonParameters</span></span>
<span data-ttu-id="8887e-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8887e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8887e-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8887e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8887e-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8887e-143">INPUTS</span></span>

### <span data-ttu-id="8887e-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="8887e-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="8887e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8887e-145">System.String</span></span>

## <span data-ttu-id="8887e-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8887e-146">OUTPUTS</span></span>

### <span data-ttu-id="8887e-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="8887e-147">System.Object</span></span>
## <span data-ttu-id="8887e-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8887e-148">NOTES</span></span>

## <span data-ttu-id="8887e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="8887e-149">RELATED LINKS</span></span>
