---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141050"
---
# <span data-ttu-id="f79b1-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f79b1-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f79b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f79b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f79b1-103">建立資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f79b1-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f79b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f79b1-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f79b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f79b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f79b1-106">**新的-AzDataLakeAnalyticsAccount** Cmdlet 會建立 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f79b1-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f79b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="f79b1-107">EXAMPLES</span></span>

### <span data-ttu-id="f79b1-108">範例1：建立資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="f79b1-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="f79b1-109">這個命令會在名為 ContosoOrg 的資源群組中，建立一個名為 ContosoAdlAccount 的資料 Lake Analytics 帳戶，該帳戶會使用 ContosoAdlStore 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="f79b1-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="f79b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f79b1-110">PARAMETERS</span></span>

### <span data-ttu-id="f79b1-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f79b1-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="f79b1-112">指定要設定為預設資料來源的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f79b1-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79b1-113">-DefaultProfile</span></span>
<span data-ttu-id="f79b1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f79b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f79b1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f79b1-115">-Location</span></span>
<span data-ttu-id="f79b1-116">指定建立資料 Lake Analytics 帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="f79b1-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="f79b1-117">目前僅支援東美國2。</span><span class="sxs-lookup"><span data-stu-id="f79b1-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79b1-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="f79b1-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="f79b1-119">此帳戶的選用最大支援分析單位。</span><span class="sxs-lookup"><span data-stu-id="f79b1-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79b1-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="f79b1-120">-MaxJobCount</span></span>
<span data-ttu-id="f79b1-121">同時在帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="f79b1-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="f79b1-122">如果沒有指定，則預設為3</span><span class="sxs-lookup"><span data-stu-id="f79b1-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="f79b1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f79b1-123">-Name</span></span>
<span data-ttu-id="f79b1-124">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f79b1-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f79b1-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="f79b1-125">-QueryStoreRetention</span></span>
<span data-ttu-id="f79b1-126">保留作業中繼資料的可選天數。</span><span class="sxs-lookup"><span data-stu-id="f79b1-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="f79b1-127">如果沒有指定，則預設值為30天。</span><span class="sxs-lookup"><span data-stu-id="f79b1-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="f79b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="f79b1-129">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f79b1-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="f79b1-130">若要建立資源群組，請使用 New-AzResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f79b1-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="f79b1-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f79b1-131">-Tag</span></span>
<span data-ttu-id="f79b1-132">與此帳戶相關聯之標記的字串字典</span><span class="sxs-lookup"><span data-stu-id="f79b1-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79b1-133">層級</span><span class="sxs-lookup"><span data-stu-id="f79b1-133">-Tier</span></span>
<span data-ttu-id="f79b1-134">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="f79b1-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79b1-135">CommonParameters</span></span>
<span data-ttu-id="f79b1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f79b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79b1-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f79b1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79b1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f79b1-138">INPUTS</span></span>

### <span data-ttu-id="f79b1-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f79b1-139">System.String</span></span>

### <span data-ttu-id="f79b1-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f79b1-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f79b1-141">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f79b1-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f79b1-142">"DataLake" 1 [[TierType，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="f79b1-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f79b1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="f79b1-143">OUTPUTS</span></span>

### <span data-ttu-id="f79b1-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f79b1-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f79b1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="f79b1-145">NOTES</span></span>

## <span data-ttu-id="f79b1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f79b1-146">RELATED LINKS</span></span>

[<span data-ttu-id="f79b1-147">AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f79b1-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f79b1-148">移除-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f79b1-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f79b1-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f79b1-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f79b1-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f79b1-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


