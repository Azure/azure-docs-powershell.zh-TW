---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448704"
---
# <span data-ttu-id="1610e-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1610e-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1610e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1610e-102">SYNOPSIS</span></span>
<span data-ttu-id="1610e-103">修改資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1610e-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1610e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1610e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1610e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1610e-105">DESCRIPTION</span></span>
<span data-ttu-id="1610e-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會修改 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1610e-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1610e-107">示例</span><span class="sxs-lookup"><span data-stu-id="1610e-107">EXAMPLES</span></span>

### <span data-ttu-id="1610e-108">範例1：修改帳戶的資料來源</span><span class="sxs-lookup"><span data-stu-id="1610e-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="1610e-109">這個命令會變更帳戶的 [預設資料來源] 和 [Tags] 屬性。</span><span class="sxs-lookup"><span data-stu-id="1610e-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="1610e-110">參數</span><span class="sxs-lookup"><span data-stu-id="1610e-110">PARAMETERS</span></span>

### <span data-ttu-id="1610e-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="1610e-111">-AllowAzureIpState</span></span>
<span data-ttu-id="1610e-112">選擇性地透過防火牆允許/封鎖 Azure 原始 Ip。</span><span class="sxs-lookup"><span data-stu-id="1610e-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1610e-113">-DefaultProfile</span></span>
<span data-ttu-id="1610e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1610e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="1610e-115">-FirewallState</span></span>
<span data-ttu-id="1610e-116">或者，您可以選擇啟用/停用現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="1610e-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="1610e-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="1610e-118">要用來更新帳戶的選用最大支援分析單元。</span><span class="sxs-lookup"><span data-stu-id="1610e-118">The optional maximum supported analytics units to update the account with.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="1610e-119">-MaxJobCount</span></span>
<span data-ttu-id="1610e-120">在要設定的帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="1610e-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1610e-121">-Name</span></span>
<span data-ttu-id="1610e-122">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1610e-122">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="1610e-123">-QueryStoreRetention</span></span>
<span data-ttu-id="1610e-124">保留作業中繼資料以在帳戶中設定的天數（可選天數）。</span><span class="sxs-lookup"><span data-stu-id="1610e-124">The optional number of days that job metadata is retained to set in the account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1610e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1610e-126">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1610e-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1610e-127">-Tag</span></span>
<span data-ttu-id="1610e-128">與此帳戶相關聯的標籤字串字典，應取代目前的一組標記</span><span class="sxs-lookup"><span data-stu-id="1610e-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-129">層級</span><span class="sxs-lookup"><span data-stu-id="1610e-129">-Tier</span></span>
<span data-ttu-id="1610e-130">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="1610e-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1610e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1610e-131">CommonParameters</span></span>
<span data-ttu-id="1610e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1610e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1610e-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1610e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1610e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1610e-134">INPUTS</span></span>

### <span data-ttu-id="1610e-135">所有</span><span class="sxs-lookup"><span data-stu-id="1610e-135">None</span></span>
<span data-ttu-id="1610e-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1610e-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1610e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1610e-137">OUTPUTS</span></span>

### <span data-ttu-id="1610e-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1610e-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="1610e-139">更新的帳戶詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1610e-139">The updated account details.</span></span>

## <span data-ttu-id="1610e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1610e-140">NOTES</span></span>

## <span data-ttu-id="1610e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="1610e-141">RELATED LINKS</span></span>

[<span data-ttu-id="1610e-142">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1610e-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1610e-143">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1610e-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1610e-144">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1610e-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1610e-145">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1610e-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


