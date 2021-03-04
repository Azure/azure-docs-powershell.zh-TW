---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 6867e57e5465ddab8fc7f0adbfdb3197d8ac1245
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914021"
---
# <span data-ttu-id="ea82d-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ea82d-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="ea82d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea82d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea82d-103">獲得 Data Lake Analytics 計算策略或計算策略清單。</span><span class="sxs-lookup"><span data-stu-id="ea82d-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="ea82d-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea82d-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea82d-105">描述</span><span class="sxs-lookup"><span data-stu-id="ea82d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea82d-106">**Get-AzDataLakeAnalyticsComputePolicy** 會取得指定的 Azure Data Lake Analytics 計算策略或策略清單。</span><span class="sxs-lookup"><span data-stu-id="ea82d-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="ea82d-107">例子</span><span class="sxs-lookup"><span data-stu-id="ea82d-107">EXAMPLES</span></span>

### <span data-ttu-id="ea82d-108">範例 1：取得指定的計算策略</span><span class="sxs-lookup"><span data-stu-id="ea82d-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="ea82d-109">此命令會獲得帳戶 'contodla' 中名稱為 "myPolicy" 的指定計算策略。</span><span class="sxs-lookup"><span data-stu-id="ea82d-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="ea82d-110">範例 2：取得帳戶內所有計算策略的清單</span><span class="sxs-lookup"><span data-stu-id="ea82d-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="ea82d-111">此命令會獲得帳戶 "contodla" 中所有計算策略的清單</span><span class="sxs-lookup"><span data-stu-id="ea82d-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="ea82d-112">參數</span><span class="sxs-lookup"><span data-stu-id="ea82d-112">PARAMETERS</span></span>

### <span data-ttu-id="ea82d-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ea82d-113">-Account</span></span>
<span data-ttu-id="ea82d-114">取得計算策略或策略之帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea82d-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="ea82d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea82d-115">-DefaultProfile</span></span>
<span data-ttu-id="ea82d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ea82d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea82d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea82d-117">-Name</span></span>
<span data-ttu-id="ea82d-118">要取得的計算策略名稱。</span><span class="sxs-lookup"><span data-stu-id="ea82d-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="ea82d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea82d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea82d-120">您帳戶存在下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ea82d-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="ea82d-121">選擇性，並嘗試探索是否未提供。</span><span class="sxs-lookup"><span data-stu-id="ea82d-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="ea82d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea82d-122">CommonParameters</span></span>
<span data-ttu-id="ea82d-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea82d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea82d-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ea82d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea82d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ea82d-125">INPUTS</span></span>

### <span data-ttu-id="ea82d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ea82d-126">System.String</span></span>

## <span data-ttu-id="ea82d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ea82d-127">OUTPUTS</span></span>

### <span data-ttu-id="ea82d-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ea82d-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="ea82d-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ea82d-129">NOTES</span></span>

## <span data-ttu-id="ea82d-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea82d-130">RELATED LINKS</span></span>
