---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: dcd44f9b43184ffc36d58bd5b65a065d7e81b4b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905117"
---
# <span data-ttu-id="a81af-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a81af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a81af-102">SYNOPSIS</span></span>
<span data-ttu-id="a81af-103">獲得 Data Lake Analytics 帳戶相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a81af-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a81af-104">語法</span><span class="sxs-lookup"><span data-stu-id="a81af-104">SYNTAX</span></span>

### <span data-ttu-id="a81af-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="a81af-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81af-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a81af-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a81af-107">GetByS0ificAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a81af-108">描述</span><span class="sxs-lookup"><span data-stu-id="a81af-108">DESCRIPTION</span></span>
<span data-ttu-id="a81af-109">**Get-AzDataLakeAnalyticsAccount** Cmdlet 會取得 Azure Data Lake Analytics 帳戶相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a81af-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a81af-110">例子</span><span class="sxs-lookup"><span data-stu-id="a81af-110">EXAMPLES</span></span>

### <span data-ttu-id="a81af-111">範例 1：取得 Data Lake Analytics 帳戶相關資訊</span><span class="sxs-lookup"><span data-stu-id="a81af-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="a81af-112">此命令會獲得名為 ContosoAdlAccount的帳戶相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a81af-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="a81af-113">參數</span><span class="sxs-lookup"><span data-stu-id="a81af-113">PARAMETERS</span></span>

### <span data-ttu-id="a81af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81af-114">-DefaultProfile</span></span>
<span data-ttu-id="a81af-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a81af-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a81af-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a81af-116">-Name</span></span>
<span data-ttu-id="a81af-117">指定 Data Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a81af-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a81af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a81af-118">-ResourceGroupName</span></span>
<span data-ttu-id="a81af-119">指定 Data Lake Analytics 帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a81af-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a81af-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81af-120">CommonParameters</span></span>
<span data-ttu-id="a81af-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a81af-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81af-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a81af-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81af-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a81af-123">INPUTS</span></span>

### <span data-ttu-id="a81af-124">System.String</span><span class="sxs-lookup"><span data-stu-id="a81af-124">System.String</span></span>

## <span data-ttu-id="a81af-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a81af-125">OUTPUTS</span></span>

### <span data-ttu-id="a81af-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="a81af-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="a81af-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="a81af-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a81af-128">NOTES</span></span>

## <span data-ttu-id="a81af-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a81af-129">RELATED LINKS</span></span>

[<span data-ttu-id="a81af-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a81af-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a81af-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a81af-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a81af-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


