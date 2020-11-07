---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4f3ffda3bbac6658cf54af1c7b459ce70f651e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626309"
---
# <span data-ttu-id="43522-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="43522-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="43522-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43522-102">SYNOPSIS</span></span>
<span data-ttu-id="43522-103">檢查是否存在資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="43522-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43522-104">句法</span><span class="sxs-lookup"><span data-stu-id="43522-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43522-105">說明</span><span class="sxs-lookup"><span data-stu-id="43522-105">DESCRIPTION</span></span>
<span data-ttu-id="43522-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會檢查是否存在資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="43522-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="43522-107">示例</span><span class="sxs-lookup"><span data-stu-id="43522-107">EXAMPLES</span></span>

### <span data-ttu-id="43522-108">範例1：測試帳戶是否存在</span><span class="sxs-lookup"><span data-stu-id="43522-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="43522-109">這個命令會測試名為 ContosoAdlAccount 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="43522-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="43522-110">參數</span><span class="sxs-lookup"><span data-stu-id="43522-110">PARAMETERS</span></span>

### <span data-ttu-id="43522-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="43522-111">-Name</span></span>
<span data-ttu-id="43522-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="43522-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="43522-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43522-113">-ResourceGroupName</span></span>
<span data-ttu-id="43522-114">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="43522-114">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="43522-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43522-115">-DefaultProfile</span></span>
<span data-ttu-id="43522-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43522-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43522-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43522-117">CommonParameters</span></span>
<span data-ttu-id="43522-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43522-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43522-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43522-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43522-120">輸入</span><span class="sxs-lookup"><span data-stu-id="43522-120">INPUTS</span></span>

## <span data-ttu-id="43522-121">輸出</span><span class="sxs-lookup"><span data-stu-id="43522-121">OUTPUTS</span></span>

### <span data-ttu-id="43522-122">bool</span><span class="sxs-lookup"><span data-stu-id="43522-122">bool</span></span>
<span data-ttu-id="43522-123">True 或 false，表示帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="43522-123">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="43522-124">筆記</span><span class="sxs-lookup"><span data-stu-id="43522-124">NOTES</span></span>

## <span data-ttu-id="43522-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="43522-125">RELATED LINKS</span></span>

[<span data-ttu-id="43522-126">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="43522-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="43522-127">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="43522-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="43522-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="43522-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


