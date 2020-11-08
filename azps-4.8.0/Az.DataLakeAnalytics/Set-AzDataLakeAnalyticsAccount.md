---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2a762bb115132f97dd31cf14f9f13d7c6cf5ef70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971140"
---
# <span data-ttu-id="edbfc-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="edbfc-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="edbfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="edbfc-103">修改資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="edbfc-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="edbfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="edbfc-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edbfc-105">說明</span><span class="sxs-lookup"><span data-stu-id="edbfc-105">DESCRIPTION</span></span>
<span data-ttu-id="edbfc-106">**AzDataLakeAnalyticsAccount** Cmdlet 會修改 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="edbfc-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="edbfc-107">示例</span><span class="sxs-lookup"><span data-stu-id="edbfc-107">EXAMPLES</span></span>

### <span data-ttu-id="edbfc-108">範例1：修改帳戶的資料來源</span><span class="sxs-lookup"><span data-stu-id="edbfc-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="edbfc-109">這個命令會變更帳戶的 [預設資料來源] 和 [Tags] 屬性。</span><span class="sxs-lookup"><span data-stu-id="edbfc-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="edbfc-110">參數</span><span class="sxs-lookup"><span data-stu-id="edbfc-110">PARAMETERS</span></span>

### <span data-ttu-id="edbfc-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="edbfc-111">-AllowAzureIpState</span></span>
<span data-ttu-id="edbfc-112">選擇性地透過防火牆允許/封鎖 Azure 原始 Ip。</span><span class="sxs-lookup"><span data-stu-id="edbfc-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbfc-113">-DefaultProfile</span></span>
<span data-ttu-id="edbfc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="edbfc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edbfc-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="edbfc-115">-FirewallState</span></span>
<span data-ttu-id="edbfc-116">或者，您可以選擇啟用/停用現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="edbfc-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbfc-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="edbfc-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="edbfc-118">要用來更新帳戶的選用最大支援分析單元。</span><span class="sxs-lookup"><span data-stu-id="edbfc-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="edbfc-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="edbfc-119">-MaxJobCount</span></span>
<span data-ttu-id="edbfc-120">在要設定的帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="edbfc-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="edbfc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="edbfc-121">-Name</span></span>
<span data-ttu-id="edbfc-122">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="edbfc-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="edbfc-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="edbfc-123">-QueryStoreRetention</span></span>
<span data-ttu-id="edbfc-124">保留作業中繼資料以在帳戶中設定的天數（可選天數）。</span><span class="sxs-lookup"><span data-stu-id="edbfc-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="edbfc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbfc-125">-ResourceGroupName</span></span>
<span data-ttu-id="edbfc-126">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="edbfc-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbfc-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="edbfc-127">-Tag</span></span>
<span data-ttu-id="edbfc-128">與此帳戶相關聯的標籤字串字典，應取代目前的一組標記</span><span class="sxs-lookup"><span data-stu-id="edbfc-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbfc-129">層級</span><span class="sxs-lookup"><span data-stu-id="edbfc-129">-Tier</span></span>
<span data-ttu-id="edbfc-130">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="edbfc-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="edbfc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbfc-131">CommonParameters</span></span>
<span data-ttu-id="edbfc-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edbfc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbfc-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edbfc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbfc-134">輸入</span><span class="sxs-lookup"><span data-stu-id="edbfc-134">INPUTS</span></span>

### <span data-ttu-id="edbfc-135">System.object</span><span class="sxs-lookup"><span data-stu-id="edbfc-135">System.String</span></span>

### <span data-ttu-id="edbfc-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="edbfc-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="edbfc-137">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="edbfc-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="edbfc-138">"DataLake" 1 [[TierType，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="edbfc-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="edbfc-139">"DataLake" 1 [[FirewallState，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="edbfc-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="edbfc-140">"DataLake" 1 [[FirewallAllowAzureIpsState，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="edbfc-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="edbfc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="edbfc-141">OUTPUTS</span></span>

### <span data-ttu-id="edbfc-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="edbfc-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="edbfc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="edbfc-143">NOTES</span></span>

## <span data-ttu-id="edbfc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="edbfc-144">RELATED LINKS</span></span>

[<span data-ttu-id="edbfc-145">AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="edbfc-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="edbfc-146">新-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="edbfc-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="edbfc-147">移除-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="edbfc-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="edbfc-148">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="edbfc-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


