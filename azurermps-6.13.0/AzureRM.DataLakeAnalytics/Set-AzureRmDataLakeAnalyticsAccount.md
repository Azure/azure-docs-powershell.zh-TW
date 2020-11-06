---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4bfbb25fa8b1e372175f741fd298384caa8050ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451264"
---
# <span data-ttu-id="47b5a-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="47b5a-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="47b5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="47b5a-103">修改資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="47b5a-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47b5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="47b5a-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="47b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="47b5a-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會修改 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="47b5a-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="47b5a-107">示例</span><span class="sxs-lookup"><span data-stu-id="47b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="47b5a-108">範例1：修改帳戶的資料來源</span><span class="sxs-lookup"><span data-stu-id="47b5a-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="47b5a-109">這個命令會變更帳戶的 [預設資料來源] 和 [Tags] 屬性。</span><span class="sxs-lookup"><span data-stu-id="47b5a-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="47b5a-110">參數</span><span class="sxs-lookup"><span data-stu-id="47b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="47b5a-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="47b5a-111">-AllowAzureIpState</span></span>
<span data-ttu-id="47b5a-112">選擇性地透過防火牆允許/封鎖 Azure 原始 Ip。</span><span class="sxs-lookup"><span data-stu-id="47b5a-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="47b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="47b5a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="47b5a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47b5a-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="47b5a-115">-FirewallState</span></span>
<span data-ttu-id="47b5a-116">或者，您可以選擇啟用/停用現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="47b5a-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="47b5a-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="47b5a-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="47b5a-118">要用來更新帳戶的選用最大支援分析單元。</span><span class="sxs-lookup"><span data-stu-id="47b5a-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="47b5a-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="47b5a-119">-MaxJobCount</span></span>
<span data-ttu-id="47b5a-120">在要設定的帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="47b5a-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="47b5a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="47b5a-121">-Name</span></span>
<span data-ttu-id="47b5a-122">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="47b5a-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="47b5a-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="47b5a-123">-QueryStoreRetention</span></span>
<span data-ttu-id="47b5a-124">保留作業中繼資料以在帳戶中設定的天數（可選天數）。</span><span class="sxs-lookup"><span data-stu-id="47b5a-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="47b5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="47b5a-126">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="47b5a-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="47b5a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="47b5a-127">-Tag</span></span>
<span data-ttu-id="47b5a-128">與此帳戶相關聯的標籤字串字典，應取代目前的一組標記</span><span class="sxs-lookup"><span data-stu-id="47b5a-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="47b5a-129">層級</span><span class="sxs-lookup"><span data-stu-id="47b5a-129">-Tier</span></span>
<span data-ttu-id="47b5a-130">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="47b5a-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="47b5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b5a-131">CommonParameters</span></span>
<span data-ttu-id="47b5a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47b5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b5a-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47b5a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b5a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="47b5a-134">INPUTS</span></span>

### <span data-ttu-id="47b5a-135">System.object</span><span class="sxs-lookup"><span data-stu-id="47b5a-135">System.String</span></span>

### <span data-ttu-id="47b5a-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47b5a-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="47b5a-137">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="47b5a-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="47b5a-138">"DataLake" 1 [[TierType，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="47b5a-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="47b5a-139">"DataLake" 1 [[FirewallState，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="47b5a-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="47b5a-140">"DataLake" 1 [[FirewallAllowAzureIpsState，DataLake.. 分析，版本 = 3.0.0.0 版，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="47b5a-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="47b5a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="47b5a-141">OUTPUTS</span></span>

### <span data-ttu-id="47b5a-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="47b5a-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="47b5a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="47b5a-143">NOTES</span></span>

## <span data-ttu-id="47b5a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="47b5a-144">RELATED LINKS</span></span>

[<span data-ttu-id="47b5a-145">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="47b5a-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="47b5a-146">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="47b5a-146">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="47b5a-147">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="47b5a-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="47b5a-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="47b5a-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


