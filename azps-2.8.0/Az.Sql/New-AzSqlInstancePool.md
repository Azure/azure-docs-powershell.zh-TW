---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: d65e32992b113dfb587b68dd3fcdc1701b291ad4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792717"
---
# <span data-ttu-id="5778d-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="5778d-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="5778d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5778d-102">SYNOPSIS</span></span>
<span data-ttu-id="5778d-103">建立 Azure SQL 實例池。</span><span class="sxs-lookup"><span data-stu-id="5778d-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5778d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5778d-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5778d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5778d-105">DESCRIPTION</span></span>
<span data-ttu-id="5778d-106">**新的-AzSqlInstancePool** Cmdlet 會建立 Azure SQL 實例池。</span><span class="sxs-lookup"><span data-stu-id="5778d-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5778d-107">示例</span><span class="sxs-lookup"><span data-stu-id="5778d-107">EXAMPLES</span></span>

### <span data-ttu-id="5778d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5778d-108">Example 1</span></span>
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

<span data-ttu-id="5778d-109">這個命令會建立新的 Azure SQL 實例池。</span><span class="sxs-lookup"><span data-stu-id="5778d-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5778d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5778d-110">PARAMETERS</span></span>

### <span data-ttu-id="5778d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5778d-111">-AsJob</span></span>
<span data-ttu-id="5778d-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5778d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5778d-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5778d-113">-ComputeGeneration</span></span>
<span data-ttu-id="5778d-114">為實例池所產生的計算。</span><span class="sxs-lookup"><span data-stu-id="5778d-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="5778d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5778d-115">-DefaultProfile</span></span>
<span data-ttu-id="5778d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5778d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5778d-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="5778d-117">-Edition</span></span>
<span data-ttu-id="5778d-118">實例池的版本。</span><span class="sxs-lookup"><span data-stu-id="5778d-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="5778d-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5778d-119">-LicenseType</span></span>
<span data-ttu-id="5778d-120">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="5778d-120">Determines which License Type to use.</span></span>
<span data-ttu-id="5778d-121">可能的值為 BasePrice (，AHB 折扣) 和 LicenseIncluded (沒有 AHB 的折扣) 。</span><span class="sxs-lookup"><span data-stu-id="5778d-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="5778d-122">-位置</span><span class="sxs-lookup"><span data-stu-id="5778d-122">-Location</span></span>
<span data-ttu-id="5778d-123">建立實例池的位置。</span><span class="sxs-lookup"><span data-stu-id="5778d-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="5778d-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5778d-124">-Name</span></span>
<span data-ttu-id="5778d-125">實例池的名稱。</span><span class="sxs-lookup"><span data-stu-id="5778d-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="5778d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5778d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5778d-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5778d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="5778d-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5778d-128">-SubnetId</span></span>
<span data-ttu-id="5778d-129">要用於建立實例池的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="5778d-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="5778d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="5778d-130">-Tag</span></span>
<span data-ttu-id="5778d-131">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="5778d-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="5778d-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="5778d-132">-VCore</span></span>
<span data-ttu-id="5778d-133">決定要與實例關聯的 VCore 量。</span><span class="sxs-lookup"><span data-stu-id="5778d-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="5778d-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5778d-134">-Confirm</span></span>
<span data-ttu-id="5778d-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5778d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5778d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5778d-136">-WhatIf</span></span>
<span data-ttu-id="5778d-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5778d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5778d-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5778d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5778d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5778d-139">CommonParameters</span></span>
<span data-ttu-id="5778d-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5778d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5778d-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5778d-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5778d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5778d-142">INPUTS</span></span>

### <span data-ttu-id="5778d-143">所有</span><span class="sxs-lookup"><span data-stu-id="5778d-143">None</span></span>

## <span data-ttu-id="5778d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="5778d-144">OUTPUTS</span></span>

### <span data-ttu-id="5778d-145">System.object</span><span class="sxs-lookup"><span data-stu-id="5778d-145">System.Object</span></span>
## <span data-ttu-id="5778d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="5778d-146">NOTES</span></span>

## <span data-ttu-id="5778d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="5778d-147">RELATED LINKS</span></span>
