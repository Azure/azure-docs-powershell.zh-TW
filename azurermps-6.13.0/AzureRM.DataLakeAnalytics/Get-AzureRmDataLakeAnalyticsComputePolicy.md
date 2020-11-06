---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8a563f6cbb7faeb124fb0b93ed468a368c2556eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453807"
---
# <span data-ttu-id="8c986-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8c986-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8c986-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c986-102">SYNOPSIS</span></span>
<span data-ttu-id="8c986-103">取得資料 Lake Analytics 計算原則或計算原則清單。</span><span class="sxs-lookup"><span data-stu-id="8c986-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c986-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c986-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c986-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c986-105">DESCRIPTION</span></span>
<span data-ttu-id="8c986-106">**AzureRmDataLakeAnalyticsComputePolicy** 會取得指定的 Azure Data Lake Analytics 計算原則或原則清單。</span><span class="sxs-lookup"><span data-stu-id="8c986-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="8c986-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c986-107">EXAMPLES</span></span>

### <span data-ttu-id="8c986-108">範例1：取得指定的計算原則</span><span class="sxs-lookup"><span data-stu-id="8c986-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="8c986-109">這個命令會取得帳戶 "contosoadla" 中名為 "myPolicy" 的指定計算原則。</span><span class="sxs-lookup"><span data-stu-id="8c986-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="8c986-110">範例2：取得帳戶中的所有計算原則清單</span><span class="sxs-lookup"><span data-stu-id="8c986-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="8c986-111">這個命令會取得帳戶 "contosoadla" 中所有計算原則的清單</span><span class="sxs-lookup"><span data-stu-id="8c986-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="8c986-112">參數</span><span class="sxs-lookup"><span data-stu-id="8c986-112">PARAMETERS</span></span>

### <span data-ttu-id="8c986-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="8c986-113">-Account</span></span>
<span data-ttu-id="8c986-114">要從中取得計算原則或原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8c986-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="8c986-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c986-115">-DefaultProfile</span></span>
<span data-ttu-id="8c986-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8c986-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c986-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c986-117">-Name</span></span>
<span data-ttu-id="8c986-118">要取得之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c986-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c986-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c986-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c986-120">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c986-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="8c986-121">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="8c986-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="8c986-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c986-122">CommonParameters</span></span>
<span data-ttu-id="8c986-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c986-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c986-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c986-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c986-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8c986-125">INPUTS</span></span>

### <span data-ttu-id="8c986-126">System.object</span><span class="sxs-lookup"><span data-stu-id="8c986-126">System.String</span></span>

## <span data-ttu-id="8c986-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8c986-127">OUTPUTS</span></span>

### <span data-ttu-id="8c986-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8c986-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8c986-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8c986-129">NOTES</span></span>

## <span data-ttu-id="8c986-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c986-130">RELATED LINKS</span></span>
