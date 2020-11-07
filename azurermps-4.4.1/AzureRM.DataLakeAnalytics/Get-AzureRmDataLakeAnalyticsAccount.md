---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623670"
---
# <span data-ttu-id="0a0bd-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a0bd-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0a0bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0bd-103">取得資料 Lake Analytics 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a0bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a0bd-104">SYNTAX</span></span>

### <span data-ttu-id="0a0bd-105">[全部在訂閱] 中 (預設) </span><span class="sxs-lookup"><span data-stu-id="0a0bd-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a0bd-106">[資源群組] 中的 [全部]</span><span class="sxs-lookup"><span data-stu-id="0a0bd-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a0bd-107">特定帳戶</span><span class="sxs-lookup"><span data-stu-id="0a0bd-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a0bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="0a0bd-108">DESCRIPTION</span></span>
<span data-ttu-id="0a0bd-109">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會取得 Azure Data Lake Analytics 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0a0bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a0bd-110">EXAMPLES</span></span>

### <span data-ttu-id="0a0bd-111">範例1：取得資料 Lake Analytics 帳戶的相關資訊</span><span class="sxs-lookup"><span data-stu-id="0a0bd-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0a0bd-112">這個命令會取得名為 ContosoAdlAccount 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="0a0bd-113">參數</span><span class="sxs-lookup"><span data-stu-id="0a0bd-113">PARAMETERS</span></span>

### <span data-ttu-id="0a0bd-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a0bd-114">-Name</span></span>
<span data-ttu-id="0a0bd-115">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0bd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0bd-116">-ResourceGroupName</span></span>
<span data-ttu-id="0a0bd-117">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0bd-118">-DefaultProfile</span></span>
<span data-ttu-id="0a0bd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a0bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0bd-120">CommonParameters</span></span>
<span data-ttu-id="0a0bd-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0bd-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0bd-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0a0bd-123">INPUTS</span></span>

## <span data-ttu-id="0a0bd-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0a0bd-124">OUTPUTS</span></span>

### <span data-ttu-id="0a0bd-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a0bd-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="0a0bd-126">指定的帳號詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-126">The specified account details.</span></span>

### <span data-ttu-id="0a0bd-127">清單<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="0a0bd-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="0a0bd-128">指定資源群組或訂閱中的帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="0a0bd-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="0a0bd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0a0bd-129">NOTES</span></span>

## <span data-ttu-id="0a0bd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a0bd-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a0bd-131">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a0bd-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a0bd-132">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a0bd-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a0bd-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a0bd-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a0bd-134">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a0bd-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


