---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453784"
---
# <span data-ttu-id="f2774-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f2774-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f2774-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2774-102">SYNOPSIS</span></span>
<span data-ttu-id="f2774-103">建立資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f2774-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2774-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2774-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2774-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2774-105">DESCRIPTION</span></span>
<span data-ttu-id="f2774-106">**新的-AzureRmDataLakeAnalyticsAccount** Cmdlet 會建立 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f2774-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2774-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2774-107">EXAMPLES</span></span>

### <span data-ttu-id="f2774-108">範例1：建立資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="f2774-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="f2774-109">這個命令會在名為 ContosoOrg 的資源群組中，建立一個名為 ContosoAdlAccount 的資料 Lake Analytics 帳戶，該帳戶會使用 ContosoAdlStore 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="f2774-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="f2774-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2774-110">PARAMETERS</span></span>

### <span data-ttu-id="f2774-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f2774-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="f2774-112">指定要設定為預設資料來源的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f2774-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="f2774-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2774-113">-DefaultProfile</span></span>
<span data-ttu-id="f2774-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f2774-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2774-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f2774-115">-Location</span></span>
<span data-ttu-id="f2774-116">指定建立資料 Lake Analytics 帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="f2774-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="f2774-117">目前僅支援東美國2。</span><span class="sxs-lookup"><span data-stu-id="f2774-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="f2774-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="f2774-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="f2774-119">此帳戶的選用最大支援分析單位。</span><span class="sxs-lookup"><span data-stu-id="f2774-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="f2774-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="f2774-120">-MaxJobCount</span></span>
<span data-ttu-id="f2774-121">同時在帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="f2774-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="f2774-122">如果沒有指定，則預設為3</span><span class="sxs-lookup"><span data-stu-id="f2774-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="f2774-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2774-123">-Name</span></span>
<span data-ttu-id="f2774-124">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f2774-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f2774-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="f2774-125">-QueryStoreRetention</span></span>
<span data-ttu-id="f2774-126">保留作業中繼資料的可選天數。</span><span class="sxs-lookup"><span data-stu-id="f2774-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="f2774-127">如果沒有指定，則預設值為30天。</span><span class="sxs-lookup"><span data-stu-id="f2774-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="f2774-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2774-128">-ResourceGroupName</span></span>
<span data-ttu-id="f2774-129">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f2774-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="f2774-130">若要建立資源群組，請使用 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2774-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="f2774-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2774-131">-Tag</span></span>
<span data-ttu-id="f2774-132">與此帳戶相關聯之標記的字串字典</span><span class="sxs-lookup"><span data-stu-id="f2774-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="f2774-133">層級</span><span class="sxs-lookup"><span data-stu-id="f2774-133">-Tier</span></span>
<span data-ttu-id="f2774-134">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="f2774-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="f2774-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2774-135">CommonParameters</span></span>
<span data-ttu-id="f2774-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2774-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2774-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2774-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2774-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f2774-138">INPUTS</span></span>

### <span data-ttu-id="f2774-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f2774-139">System.String</span></span>

### <span data-ttu-id="f2774-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2774-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f2774-141">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f2774-141">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f2774-142">"DataLake" 1 [[TierType，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="f2774-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f2774-143">輸出</span><span class="sxs-lookup"><span data-stu-id="f2774-143">OUTPUTS</span></span>

### <span data-ttu-id="f2774-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f2774-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f2774-145">筆記</span><span class="sxs-lookup"><span data-stu-id="f2774-145">NOTES</span></span>

## <span data-ttu-id="f2774-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2774-146">RELATED LINKS</span></span>

[<span data-ttu-id="f2774-147">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f2774-147">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f2774-148">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f2774-148">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f2774-149">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f2774-149">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f2774-150">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f2774-150">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


