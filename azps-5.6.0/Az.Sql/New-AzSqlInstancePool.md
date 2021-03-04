---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 818e76c9ea46b2593b3bdd3871f417dbaca044a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908342"
---
# <span data-ttu-id="43c45-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="43c45-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="43c45-102">簡介</span><span class="sxs-lookup"><span data-stu-id="43c45-102">SYNOPSIS</span></span>
<span data-ttu-id="43c45-103">建立 Azure SQL 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="43c45-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="43c45-104">語法</span><span class="sxs-lookup"><span data-stu-id="43c45-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43c45-105">描述</span><span class="sxs-lookup"><span data-stu-id="43c45-105">DESCRIPTION</span></span>
<span data-ttu-id="43c45-106">**New-AzSqlInstancePool** Cmdlet 會建立 Azure SQL 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="43c45-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="43c45-107">例子</span><span class="sxs-lookup"><span data-stu-id="43c45-107">EXAMPLES</span></span>

### <span data-ttu-id="43c45-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="43c45-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
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

<span data-ttu-id="43c45-109">此命令會建立一個新的 Azure SQL 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="43c45-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="43c45-110">參數</span><span class="sxs-lookup"><span data-stu-id="43c45-110">PARAMETERS</span></span>

### <span data-ttu-id="43c45-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c45-111">-AsJob</span></span>
<span data-ttu-id="43c45-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43c45-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43c45-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="43c45-113">-ComputeGeneration</span></span>
<span data-ttu-id="43c45-114">實例資料庫的計算產生。</span><span class="sxs-lookup"><span data-stu-id="43c45-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="43c45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c45-115">-DefaultProfile</span></span>
<span data-ttu-id="43c45-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="43c45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43c45-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="43c45-117">-Edition</span></span>
<span data-ttu-id="43c45-118">實例資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="43c45-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="43c45-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="43c45-119">-LicenseType</span></span>
<span data-ttu-id="43c45-120">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="43c45-120">Determines which License Type to use.</span></span>
<span data-ttu-id="43c45-121">可能的值為 BASEPrice (具有AHB 折扣) 且 LicenseIncluded (不含AHB 折扣) 。</span><span class="sxs-lookup"><span data-stu-id="43c45-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="43c45-122">-位置</span><span class="sxs-lookup"><span data-stu-id="43c45-122">-Location</span></span>
<span data-ttu-id="43c45-123">建立實例資料庫的位置。</span><span class="sxs-lookup"><span data-stu-id="43c45-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="43c45-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="43c45-124">-Name</span></span>
<span data-ttu-id="43c45-125">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="43c45-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c45-126">-ResourceGroupName</span></span>
<span data-ttu-id="43c45-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43c45-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c45-128">-子網Id</span><span class="sxs-lookup"><span data-stu-id="43c45-128">-SubnetId</span></span>
<span data-ttu-id="43c45-129">用於建立實例資料庫的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="43c45-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="43c45-130">-標記</span><span class="sxs-lookup"><span data-stu-id="43c45-130">-Tag</span></span>
<span data-ttu-id="43c45-131">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="43c45-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="43c45-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="43c45-132">-VCore</span></span>
<span data-ttu-id="43c45-133">決定要與實例關聯多少 VCore。</span><span class="sxs-lookup"><span data-stu-id="43c45-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c45-134">-確認</span><span class="sxs-lookup"><span data-stu-id="43c45-134">-Confirm</span></span>
<span data-ttu-id="43c45-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="43c45-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c45-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c45-136">-WhatIf</span></span>
<span data-ttu-id="43c45-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43c45-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43c45-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43c45-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c45-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c45-139">CommonParameters</span></span>
<span data-ttu-id="43c45-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="43c45-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c45-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43c45-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c45-142">輸入</span><span class="sxs-lookup"><span data-stu-id="43c45-142">INPUTS</span></span>

### <span data-ttu-id="43c45-143">沒有</span><span class="sxs-lookup"><span data-stu-id="43c45-143">None</span></span>

## <span data-ttu-id="43c45-144">輸出</span><span class="sxs-lookup"><span data-stu-id="43c45-144">OUTPUTS</span></span>

### <span data-ttu-id="43c45-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="43c45-145">System.Object</span></span>
## <span data-ttu-id="43c45-146">筆記</span><span class="sxs-lookup"><span data-stu-id="43c45-146">NOTES</span></span>

## <span data-ttu-id="43c45-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="43c45-147">RELATED LINKS</span></span>
