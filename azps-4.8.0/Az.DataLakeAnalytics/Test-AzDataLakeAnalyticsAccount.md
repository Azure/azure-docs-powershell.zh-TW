---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 0f0cad155cdb274596aba449e26e82b94ca56aae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969306"
---
# <span data-ttu-id="23783-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="23783-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="23783-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23783-102">SYNOPSIS</span></span>
<span data-ttu-id="23783-103">檢查是否存在資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="23783-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="23783-104">句法</span><span class="sxs-lookup"><span data-stu-id="23783-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23783-105">說明</span><span class="sxs-lookup"><span data-stu-id="23783-105">DESCRIPTION</span></span>
<span data-ttu-id="23783-106">**AzDataLakeAnalyticsAccount** Cmdlet 會檢查是否存在資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="23783-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="23783-107">示例</span><span class="sxs-lookup"><span data-stu-id="23783-107">EXAMPLES</span></span>

### <span data-ttu-id="23783-108">範例1：測試帳戶是否存在</span><span class="sxs-lookup"><span data-stu-id="23783-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="23783-109">這個命令會測試名為 ContosoAdlAccount 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="23783-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="23783-110">參數</span><span class="sxs-lookup"><span data-stu-id="23783-110">PARAMETERS</span></span>

### <span data-ttu-id="23783-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23783-111">-DefaultProfile</span></span>
<span data-ttu-id="23783-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23783-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23783-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="23783-113">-Name</span></span>
<span data-ttu-id="23783-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="23783-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="23783-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23783-115">-ResourceGroupName</span></span>
<span data-ttu-id="23783-116">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="23783-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="23783-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23783-117">CommonParameters</span></span>
<span data-ttu-id="23783-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23783-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23783-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23783-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23783-120">輸入</span><span class="sxs-lookup"><span data-stu-id="23783-120">INPUTS</span></span>

### <span data-ttu-id="23783-121">System.object</span><span class="sxs-lookup"><span data-stu-id="23783-121">System.String</span></span>

## <span data-ttu-id="23783-122">輸出</span><span class="sxs-lookup"><span data-stu-id="23783-122">OUTPUTS</span></span>

### <span data-ttu-id="23783-123">System.object</span><span class="sxs-lookup"><span data-stu-id="23783-123">System.Boolean</span></span>

## <span data-ttu-id="23783-124">筆記</span><span class="sxs-lookup"><span data-stu-id="23783-124">NOTES</span></span>

## <span data-ttu-id="23783-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="23783-125">RELATED LINKS</span></span>

[<span data-ttu-id="23783-126">AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="23783-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="23783-127">新-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="23783-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="23783-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="23783-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


