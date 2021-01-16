---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439384"
---
# <span data-ttu-id="a9e70-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a9e70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9e70-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e70-103">取得資料 Lake Analytics 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9e70-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a9e70-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9e70-104">SYNTAX</span></span>

### <span data-ttu-id="a9e70-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="a9e70-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e70-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9e70-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9e70-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9e70-108">說明</span><span class="sxs-lookup"><span data-stu-id="a9e70-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e70-109">**AzDataLakeAnalyticsAccount** Cmdlet 會取得 Azure Data Lake Analytics 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9e70-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a9e70-110">示例</span><span class="sxs-lookup"><span data-stu-id="a9e70-110">EXAMPLES</span></span>

### <span data-ttu-id="a9e70-111">範例1：取得資料 Lake Analytics 帳戶的相關資訊</span><span class="sxs-lookup"><span data-stu-id="a9e70-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="a9e70-112">這個命令會取得名為 ContosoAdlAccount 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9e70-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="a9e70-113">參數</span><span class="sxs-lookup"><span data-stu-id="a9e70-113">PARAMETERS</span></span>

### <span data-ttu-id="a9e70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e70-114">-DefaultProfile</span></span>
<span data-ttu-id="a9e70-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a9e70-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e70-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9e70-116">-Name</span></span>
<span data-ttu-id="a9e70-117">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9e70-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e70-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e70-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9e70-119">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a9e70-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e70-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e70-120">CommonParameters</span></span>
<span data-ttu-id="a9e70-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9e70-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e70-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9e70-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e70-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a9e70-123">INPUTS</span></span>

### <span data-ttu-id="a9e70-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a9e70-124">System.String</span></span>

## <span data-ttu-id="a9e70-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a9e70-125">OUTPUTS</span></span>

### <span data-ttu-id="a9e70-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="a9e70-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="a9e70-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="a9e70-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a9e70-128">NOTES</span></span>

## <span data-ttu-id="a9e70-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9e70-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9e70-130">新-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9e70-131">移除-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9e70-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9e70-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9e70-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


