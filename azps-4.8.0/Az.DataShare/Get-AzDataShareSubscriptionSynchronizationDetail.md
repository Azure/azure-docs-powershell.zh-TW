---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129595"
---
# <span data-ttu-id="9ceed-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9ceed-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="9ceed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ceed-102">SYNOPSIS</span></span>
<span data-ttu-id="9ceed-103">取得共用訂閱之 synchonization 詳細資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9ceed-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="9ceed-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ceed-104">SYNTAX</span></span>

### <span data-ttu-id="9ceed-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9ceed-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ceed-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ceed-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ceed-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ceed-107">DESCRIPTION</span></span>
<span data-ttu-id="9ceed-108">**AzDataShareSubscriptionSynchronizationDetail** Cmdlet 提供針對共用訂閱啟動之同步處理的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ceed-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="9ceed-109">示例</span><span class="sxs-lookup"><span data-stu-id="9ceed-109">EXAMPLES</span></span>

### <span data-ttu-id="9ceed-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9ceed-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="9ceed-111">這個命令會提供在 [資料共用帳戶] WikiAds 中針對共用訂閱 AdsShareSubscription 啟動的同步處理的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9ceed-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="9ceed-112">參數</span><span class="sxs-lookup"><span data-stu-id="9ceed-112">PARAMETERS</span></span>

### <span data-ttu-id="9ceed-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ceed-113">-AccountName</span></span>
<span data-ttu-id="9ceed-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="9ceed-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ceed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ceed-115">-DefaultProfile</span></span>
<span data-ttu-id="9ceed-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ceed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ceed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ceed-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ceed-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="9ceed-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ceed-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ceed-119">-ResourceId</span></span>
<span data-ttu-id="9ceed-120">Azure 資料共用訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9ceed-120">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ceed-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9ceed-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="9ceed-122">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="9ceed-122">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ceed-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="9ceed-123">-SynchronizationId</span></span>
<span data-ttu-id="9ceed-124">共用訂閱同步處理的同步處理 id</span><span class="sxs-lookup"><span data-stu-id="9ceed-124">Synchronization id of share subscription synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ceed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ceed-125">CommonParameters</span></span>
<span data-ttu-id="9ceed-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ceed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ceed-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ceed-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ceed-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9ceed-128">INPUTS</span></span>

### <span data-ttu-id="9ceed-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9ceed-129">System.String</span></span>

## <span data-ttu-id="9ceed-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9ceed-130">OUTPUTS</span></span>

### <span data-ttu-id="9ceed-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9ceed-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="9ceed-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9ceed-132">NOTES</span></span>

## <span data-ttu-id="9ceed-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ceed-133">RELATED LINKS</span></span>
