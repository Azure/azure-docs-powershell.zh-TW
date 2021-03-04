---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 621500a20aac57b43e86f354112ad1f8a633ec32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909710"
---
# <span data-ttu-id="1292b-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1292b-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1292b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1292b-102">SYNOPSIS</span></span>
<span data-ttu-id="1292b-103">建立 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1292b-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1292b-104">語法</span><span class="sxs-lookup"><span data-stu-id="1292b-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1292b-105">描述</span><span class="sxs-lookup"><span data-stu-id="1292b-105">DESCRIPTION</span></span>
<span data-ttu-id="1292b-106">**New-AzDataLakeAnalyticsAccount** Cmdlet 會建立 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1292b-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1292b-107">例子</span><span class="sxs-lookup"><span data-stu-id="1292b-107">EXAMPLES</span></span>

### <span data-ttu-id="1292b-108">範例 1：建立 Data Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="1292b-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="1292b-109">此命令會建立名為 ContosoAdlAccount的 Data Lake Analytics 帳戶，該帳戶使用 ContosoAdlStore Data Store，位於名為 ContosoOrg 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="1292b-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="1292b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1292b-110">PARAMETERS</span></span>

### <span data-ttu-id="1292b-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1292b-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="1292b-112">指定要設為預設資料來源的資料湖市集帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1292b-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="1292b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1292b-113">-DefaultProfile</span></span>
<span data-ttu-id="1292b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1292b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1292b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="1292b-115">-Location</span></span>
<span data-ttu-id="1292b-116">指定建立 Data Lake Analytics 帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="1292b-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="1292b-117">目前僅支援美國東部 2。</span><span class="sxs-lookup"><span data-stu-id="1292b-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="1292b-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="1292b-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="1292b-119">此帳戶的選擇性支援最大分析單位。</span><span class="sxs-lookup"><span data-stu-id="1292b-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="1292b-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="1292b-120">-MaxJobCount</span></span>
<span data-ttu-id="1292b-121">同時在帳戶下所支援的選擇性工作上限。</span><span class="sxs-lookup"><span data-stu-id="1292b-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="1292b-122">如果沒有指定，預設值為 3</span><span class="sxs-lookup"><span data-stu-id="1292b-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="1292b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1292b-123">-Name</span></span>
<span data-ttu-id="1292b-124">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1292b-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1292b-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="1292b-125">-QueryStoreRetention</span></span>
<span data-ttu-id="1292b-126">保留工作中繼資料的選擇性天數。</span><span class="sxs-lookup"><span data-stu-id="1292b-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="1292b-127">如果沒有指定，預設值為 30 天。</span><span class="sxs-lookup"><span data-stu-id="1292b-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="1292b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1292b-128">-ResourceGroupName</span></span>
<span data-ttu-id="1292b-129">指定 Data Lake Analytics 帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1292b-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="1292b-130">若要建立資源群組，請使用 New-AzResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1292b-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="1292b-131">-標記</span><span class="sxs-lookup"><span data-stu-id="1292b-131">-Tag</span></span>
<span data-ttu-id="1292b-132">與此帳戶相關聯的一個字串字串字典</span><span class="sxs-lookup"><span data-stu-id="1292b-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="1292b-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="1292b-133">-Tier</span></span>
<span data-ttu-id="1292b-134">此帳戶想要使用的承諾層級。</span><span class="sxs-lookup"><span data-stu-id="1292b-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="1292b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1292b-135">CommonParameters</span></span>
<span data-ttu-id="1292b-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1292b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1292b-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1292b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1292b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1292b-138">INPUTS</span></span>

### <span data-ttu-id="1292b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1292b-139">System.String</span></span>

### <span data-ttu-id="1292b-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1292b-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1292b-141">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1292b-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1292b-142">System.Nullable'1[[Microsoft.Azure.management.DataLake.Analytics.models.TierType，Microsoft.Azure.management.DataLake.Analytics， Version=3.0.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1292b-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1292b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1292b-143">OUTPUTS</span></span>

### <span data-ttu-id="1292b-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1292b-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1292b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1292b-145">NOTES</span></span>

## <span data-ttu-id="1292b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1292b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1292b-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1292b-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1292b-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1292b-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1292b-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1292b-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1292b-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1292b-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


