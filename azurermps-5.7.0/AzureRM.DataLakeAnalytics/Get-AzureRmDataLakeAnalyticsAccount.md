---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623826"
---
# <span data-ttu-id="4fa67-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4fa67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fa67-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa67-103">取得資料 Lake Analytics 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4fa67-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fa67-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fa67-104">SYNTAX</span></span>

### <span data-ttu-id="4fa67-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="4fa67-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fa67-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fa67-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fa67-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fa67-108">說明</span><span class="sxs-lookup"><span data-stu-id="4fa67-108">DESCRIPTION</span></span>
<span data-ttu-id="4fa67-109">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會取得 Azure Data Lake Analytics 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4fa67-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4fa67-110">示例</span><span class="sxs-lookup"><span data-stu-id="4fa67-110">EXAMPLES</span></span>

### <span data-ttu-id="4fa67-111">範例1：取得資料 Lake Analytics 帳戶的相關資訊</span><span class="sxs-lookup"><span data-stu-id="4fa67-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="4fa67-112">這個命令會取得名為 ContosoAdlAccount 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4fa67-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="4fa67-113">參數</span><span class="sxs-lookup"><span data-stu-id="4fa67-113">PARAMETERS</span></span>

### <span data-ttu-id="4fa67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa67-114">-DefaultProfile</span></span>
<span data-ttu-id="4fa67-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4fa67-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa67-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fa67-116">-Name</span></span>
<span data-ttu-id="4fa67-117">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa67-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa67-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fa67-119">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa67-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa67-120">CommonParameters</span></span>
<span data-ttu-id="4fa67-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fa67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa67-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fa67-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa67-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4fa67-123">INPUTS</span></span>

### <span data-ttu-id="4fa67-124">所有</span><span class="sxs-lookup"><span data-stu-id="4fa67-124">None</span></span>
<span data-ttu-id="4fa67-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4fa67-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fa67-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4fa67-126">OUTPUTS</span></span>

### <span data-ttu-id="4fa67-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="4fa67-128">指定的帳號詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4fa67-128">The specified account details.</span></span>

### <span data-ttu-id="4fa67-129">清單<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="4fa67-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="4fa67-130">指定資源群組或訂閱中的帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="4fa67-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="4fa67-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4fa67-131">NOTES</span></span>

## <span data-ttu-id="4fa67-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fa67-132">RELATED LINKS</span></span>

[<span data-ttu-id="4fa67-133">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4fa67-134">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4fa67-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4fa67-136">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4fa67-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


