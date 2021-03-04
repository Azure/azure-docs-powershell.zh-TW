---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: c2f7dc41bc84594d1c9d7e64dc52f27a162b8be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916157"
---
# <span data-ttu-id="da97e-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="da97e-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="da97e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="da97e-102">SYNOPSIS</span></span>
<span data-ttu-id="da97e-103">瞭解共用訂閱的同步化詳細資料。</span><span class="sxs-lookup"><span data-stu-id="da97e-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="da97e-104">語法</span><span class="sxs-lookup"><span data-stu-id="da97e-104">SYNTAX</span></span>

### <span data-ttu-id="da97e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="da97e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da97e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da97e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da97e-107">描述</span><span class="sxs-lookup"><span data-stu-id="da97e-107">DESCRIPTION</span></span>
<span data-ttu-id="da97e-108">**Get-AzDataShareSubscriptionSynchronizationDetail** Cmdlet 提供針對共用訂閱啟動之同步處理的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="da97e-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="da97e-109">例子</span><span class="sxs-lookup"><span data-stu-id="da97e-109">EXAMPLES</span></span>

### <span data-ttu-id="da97e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="da97e-110">Example 1</span></span>
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

<span data-ttu-id="da97e-111">此命令提供針對資料共用帳戶 WikiAds 下的共用訂閱 AdsShareSubscription 初始化同步處理的資訊。</span><span class="sxs-lookup"><span data-stu-id="da97e-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="da97e-112">參數</span><span class="sxs-lookup"><span data-stu-id="da97e-112">PARAMETERS</span></span>

### <span data-ttu-id="da97e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da97e-113">-AccountName</span></span>
<span data-ttu-id="da97e-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="da97e-114">Azure data share account name</span></span>

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

### <span data-ttu-id="da97e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da97e-115">-DefaultProfile</span></span>
<span data-ttu-id="da97e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="da97e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da97e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da97e-117">-ResourceGroupName</span></span>
<span data-ttu-id="da97e-118">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="da97e-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="da97e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da97e-119">-ResourceId</span></span>
<span data-ttu-id="da97e-120">Azure 資料共用訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="da97e-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="da97e-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="da97e-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="da97e-122">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="da97e-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="da97e-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="da97e-123">-SynchronizationId</span></span>
<span data-ttu-id="da97e-124">共用訂閱同步處理同步處理識別碼</span><span class="sxs-lookup"><span data-stu-id="da97e-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="da97e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da97e-125">CommonParameters</span></span>
<span data-ttu-id="da97e-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="da97e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da97e-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da97e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da97e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="da97e-128">INPUTS</span></span>

### <span data-ttu-id="da97e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="da97e-129">System.String</span></span>

## <span data-ttu-id="da97e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="da97e-130">OUTPUTS</span></span>

### <span data-ttu-id="da97e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="da97e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="da97e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="da97e-132">NOTES</span></span>

## <span data-ttu-id="da97e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="da97e-133">RELATED LINKS</span></span>
