---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959547"
---
# <span data-ttu-id="113a9-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="113a9-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="113a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="113a9-102">SYNOPSIS</span></span>
<span data-ttu-id="113a9-103">取得資料 Lake Analytics 計算原則或計算原則清單。</span><span class="sxs-lookup"><span data-stu-id="113a9-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="113a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="113a9-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="113a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="113a9-105">DESCRIPTION</span></span>
<span data-ttu-id="113a9-106">**AzDataLakeAnalyticsComputePolicy** 會取得指定的 Azure Data Lake Analytics 計算原則或原則清單。</span><span class="sxs-lookup"><span data-stu-id="113a9-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="113a9-107">示例</span><span class="sxs-lookup"><span data-stu-id="113a9-107">EXAMPLES</span></span>

### <span data-ttu-id="113a9-108">範例1：取得指定的計算原則</span><span class="sxs-lookup"><span data-stu-id="113a9-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="113a9-109">這個命令會取得帳戶 "contosoadla" 中名為 "myPolicy" 的指定計算原則。</span><span class="sxs-lookup"><span data-stu-id="113a9-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="113a9-110">範例2：取得帳戶中的所有計算原則清單</span><span class="sxs-lookup"><span data-stu-id="113a9-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="113a9-111">這個命令會取得帳戶 "contosoadla" 中所有計算原則的清單</span><span class="sxs-lookup"><span data-stu-id="113a9-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="113a9-112">參數</span><span class="sxs-lookup"><span data-stu-id="113a9-112">PARAMETERS</span></span>

### <span data-ttu-id="113a9-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="113a9-113">-Account</span></span>
<span data-ttu-id="113a9-114">要從中取得計算原則或原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="113a9-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="113a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113a9-115">-DefaultProfile</span></span>
<span data-ttu-id="113a9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="113a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="113a9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="113a9-117">-Name</span></span>
<span data-ttu-id="113a9-118">要取得之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="113a9-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="113a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="113a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="113a9-120">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="113a9-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="113a9-121">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="113a9-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="113a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113a9-122">CommonParameters</span></span>
<span data-ttu-id="113a9-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="113a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113a9-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="113a9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113a9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="113a9-125">INPUTS</span></span>

### <span data-ttu-id="113a9-126">System.object</span><span class="sxs-lookup"><span data-stu-id="113a9-126">System.String</span></span>

## <span data-ttu-id="113a9-127">輸出</span><span class="sxs-lookup"><span data-stu-id="113a9-127">OUTPUTS</span></span>

### <span data-ttu-id="113a9-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="113a9-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="113a9-129">筆記</span><span class="sxs-lookup"><span data-stu-id="113a9-129">NOTES</span></span>

## <span data-ttu-id="113a9-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="113a9-130">RELATED LINKS</span></span>
