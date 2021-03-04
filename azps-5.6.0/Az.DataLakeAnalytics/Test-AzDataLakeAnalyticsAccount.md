---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b5c1303625676006929a3c2eee80f5d5961bc438
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916571"
---
# <span data-ttu-id="ff10a-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ff10a-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ff10a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff10a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff10a-103">檢查 Data Lake Analytics 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="ff10a-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ff10a-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff10a-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff10a-105">描述</span><span class="sxs-lookup"><span data-stu-id="ff10a-105">DESCRIPTION</span></span>
<span data-ttu-id="ff10a-106">**Test-AzDataLakeAnalyticsAccount** Cmdlet 會檢查 Data Lake Analytics 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="ff10a-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ff10a-107">例子</span><span class="sxs-lookup"><span data-stu-id="ff10a-107">EXAMPLES</span></span>

### <span data-ttu-id="ff10a-108">範例 1：測試帳戶是否存在</span><span class="sxs-lookup"><span data-stu-id="ff10a-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="ff10a-109">此命令會測試名為 ContosoAdlAccount 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="ff10a-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="ff10a-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff10a-110">PARAMETERS</span></span>

### <span data-ttu-id="ff10a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff10a-111">-DefaultProfile</span></span>
<span data-ttu-id="ff10a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ff10a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff10a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff10a-113">-Name</span></span>
<span data-ttu-id="ff10a-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ff10a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ff10a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff10a-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff10a-116">指定 Data Lake Analytics 帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ff10a-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff10a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff10a-117">CommonParameters</span></span>
<span data-ttu-id="ff10a-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff10a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff10a-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ff10a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff10a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ff10a-120">INPUTS</span></span>

### <span data-ttu-id="ff10a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ff10a-121">System.String</span></span>

## <span data-ttu-id="ff10a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ff10a-122">OUTPUTS</span></span>

### <span data-ttu-id="ff10a-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff10a-123">System.Boolean</span></span>

## <span data-ttu-id="ff10a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ff10a-124">NOTES</span></span>

## <span data-ttu-id="ff10a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff10a-125">RELATED LINKS</span></span>

[<span data-ttu-id="ff10a-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ff10a-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ff10a-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ff10a-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ff10a-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ff10a-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


