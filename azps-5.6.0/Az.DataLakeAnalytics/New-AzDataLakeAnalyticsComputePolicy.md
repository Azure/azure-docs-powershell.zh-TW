---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 7cd9231134b7b78d51a9a86777c54dd99e1ffa90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911126"
---
# <span data-ttu-id="f7197-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f7197-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f7197-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7197-102">SYNOPSIS</span></span>
<span data-ttu-id="f7197-103">建立特定 AAD 實體的 Data Lake Analytics 計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="f7197-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="f7197-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7197-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7197-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7197-105">DESCRIPTION</span></span>
<span data-ttu-id="f7197-106">**New-AzDataLakeAnalyticsComputePolicy** 會為 Azure Data Lake Analytics 帳戶中的特定 AAD 實體建立指定的計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="f7197-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f7197-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7197-107">EXAMPLES</span></span>

### <span data-ttu-id="f7197-108">範例 1：建立只包含一個規則的計算原則</span><span class="sxs-lookup"><span data-stu-id="f7197-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="f7197-109">此命令會針對 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的使用者，在帳戶 "contocbdla" 中建立一個稱為 "myPolicy" 的策略，以確保他們無法提交任何分析單位超過 5 個的工作。</span><span class="sxs-lookup"><span data-stu-id="f7197-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="f7197-110">範例 2：使用兩個規則集建立計算原則</span><span class="sxs-lookup"><span data-stu-id="f7197-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="f7197-111">此命令會為 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的使用者建立帳戶 "myPolicy" 的「myPolicy」，以確保他們無法提交超過 5 個分析單位或優先順序低於 100 的工作</span><span class="sxs-lookup"><span data-stu-id="f7197-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="f7197-112">參數</span><span class="sxs-lookup"><span data-stu-id="f7197-112">PARAMETERS</span></span>

### <span data-ttu-id="f7197-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f7197-113">-Account</span></span>
<span data-ttu-id="f7197-114">要新增計算策略的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f7197-114">Name of the account to add the compute policy to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7197-115">-DefaultProfile</span></span>
<span data-ttu-id="f7197-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f7197-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7197-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="f7197-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="f7197-118">此政策每個工作支援的最大分析單位。</span><span class="sxs-lookup"><span data-stu-id="f7197-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="f7197-119">您必須指定此、MinPriorityPerJob 或兩個參數。</span><span class="sxs-lookup"><span data-stu-id="f7197-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="f7197-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="f7197-121">此政策每個工作的最低支援優先順序。</span><span class="sxs-lookup"><span data-stu-id="f7197-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="f7197-122">無論是此選項、MaxAnalyticsUnitsPerJob，或必須指定這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="f7197-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7197-123">-Name</span></span>
<span data-ttu-id="f7197-124">要建立的計算策略名稱。</span><span class="sxs-lookup"><span data-stu-id="f7197-124">Name of the compute policy to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7197-125">-ObjectId</span></span>
<span data-ttu-id="f7197-126">使用者或群組的 Azure Active Directory 物件識別碼，以將原則適用。</span><span class="sxs-lookup"><span data-stu-id="f7197-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="f7197-127">-ObjectType</span></span>
<span data-ttu-id="f7197-128">傳遞之物件識別碼的 Azure Active Directory 物件類型。</span><span class="sxs-lookup"><span data-stu-id="f7197-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7197-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7197-130">您帳戶存在下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f7197-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="f7197-131">選擇性，並嘗試探索是否未提供。</span><span class="sxs-lookup"><span data-stu-id="f7197-131">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7197-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f7197-132">-Confirm</span></span>
<span data-ttu-id="f7197-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f7197-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7197-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7197-134">-WhatIf</span></span>
<span data-ttu-id="f7197-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7197-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7197-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7197-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7197-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7197-137">CommonParameters</span></span>
<span data-ttu-id="f7197-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7197-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7197-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7197-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7197-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f7197-140">INPUTS</span></span>

### <span data-ttu-id="f7197-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f7197-141">System.String</span></span>

### <span data-ttu-id="f7197-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f7197-142">System.Guid</span></span>

### <span data-ttu-id="f7197-143">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7197-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f7197-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f7197-144">OUTPUTS</span></span>

### <span data-ttu-id="f7197-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f7197-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f7197-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f7197-146">NOTES</span></span>

## <span data-ttu-id="f7197-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7197-147">RELATED LINKS</span></span>
