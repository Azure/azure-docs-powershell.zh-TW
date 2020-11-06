---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446843"
---
# <span data-ttu-id="7aa46-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7aa46-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="7aa46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7aa46-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa46-103">修改資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7aa46-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aa46-104">句法</span><span class="sxs-lookup"><span data-stu-id="7aa46-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aa46-105">說明</span><span class="sxs-lookup"><span data-stu-id="7aa46-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa46-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會修改 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7aa46-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7aa46-107">示例</span><span class="sxs-lookup"><span data-stu-id="7aa46-107">EXAMPLES</span></span>

### <span data-ttu-id="7aa46-108">範例1：修改帳戶的資料來源</span><span class="sxs-lookup"><span data-stu-id="7aa46-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="7aa46-109">這個命令會變更帳戶的 [預設資料來源] 和 [Tags] 屬性。</span><span class="sxs-lookup"><span data-stu-id="7aa46-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="7aa46-110">參數</span><span class="sxs-lookup"><span data-stu-id="7aa46-110">PARAMETERS</span></span>

### <span data-ttu-id="7aa46-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="7aa46-111">-AllowAzureIpState</span></span>
<span data-ttu-id="7aa46-112">選擇性地透過防火牆允許/封鎖 Azure 原始 Ip。</span><span class="sxs-lookup"><span data-stu-id="7aa46-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="7aa46-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="7aa46-113">-FirewallState</span></span>
<span data-ttu-id="7aa46-114">或者，您可以選擇啟用/停用現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="7aa46-114">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="7aa46-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="7aa46-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="7aa46-116">要更新帳戶的最大並行度支援度。</span><span class="sxs-lookup"><span data-stu-id="7aa46-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="7aa46-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="7aa46-117">-MaxJobCount</span></span>
<span data-ttu-id="7aa46-118">在要設定的帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="7aa46-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="7aa46-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7aa46-119">-Name</span></span>
<span data-ttu-id="7aa46-120">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7aa46-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7aa46-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="7aa46-121">-QueryStoreRetention</span></span>
<span data-ttu-id="7aa46-122">保留作業中繼資料以在帳戶中設定的天數（可選天數）。</span><span class="sxs-lookup"><span data-stu-id="7aa46-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="7aa46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa46-123">-ResourceGroupName</span></span>
<span data-ttu-id="7aa46-124">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7aa46-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="7aa46-125">-標記</span><span class="sxs-lookup"><span data-stu-id="7aa46-125">-Tags</span></span>
<span data-ttu-id="7aa46-126">指定可用於在其他 Azure 資源之間識別資料 Lake Analytics 帳戶的鍵值對。</span><span class="sxs-lookup"><span data-stu-id="7aa46-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="7aa46-127">層級</span><span class="sxs-lookup"><span data-stu-id="7aa46-127">-Tier</span></span>
<span data-ttu-id="7aa46-128">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="7aa46-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="7aa46-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa46-129">-DefaultProfile</span></span>
<span data-ttu-id="7aa46-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7aa46-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa46-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa46-131">CommonParameters</span></span>
<span data-ttu-id="7aa46-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7aa46-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa46-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7aa46-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa46-134">輸入</span><span class="sxs-lookup"><span data-stu-id="7aa46-134">INPUTS</span></span>

## <span data-ttu-id="7aa46-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7aa46-135">OUTPUTS</span></span>

### <span data-ttu-id="7aa46-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7aa46-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="7aa46-137">更新的帳戶詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7aa46-137">The updated account details.</span></span>

## <span data-ttu-id="7aa46-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7aa46-138">NOTES</span></span>

## <span data-ttu-id="7aa46-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7aa46-139">RELATED LINKS</span></span>

[<span data-ttu-id="7aa46-140">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7aa46-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7aa46-141">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7aa46-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7aa46-142">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7aa46-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7aa46-143">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7aa46-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


