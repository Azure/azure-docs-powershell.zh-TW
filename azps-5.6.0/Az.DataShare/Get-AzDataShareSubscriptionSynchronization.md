---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904493"
---
# <span data-ttu-id="be504-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="be504-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="be504-102">簡介</span><span class="sxs-lookup"><span data-stu-id="be504-102">SYNOPSIS</span></span>
<span data-ttu-id="be504-103">在共用訂閱中，獲得同步處理執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="be504-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="be504-104">語法</span><span class="sxs-lookup"><span data-stu-id="be504-104">SYNTAX</span></span>

### <span data-ttu-id="be504-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be504-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be504-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be504-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be504-107">描述</span><span class="sxs-lookup"><span data-stu-id="be504-107">DESCRIPTION</span></span>
<span data-ttu-id="be504-108">**Get-AzDataShareSubscriptionSynchronization** Cmdlet 提供在共用訂閱中，在消費者的資料共用帳戶下執行所有同步處理資訊。</span><span class="sxs-lookup"><span data-stu-id="be504-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="be504-109">例子</span><span class="sxs-lookup"><span data-stu-id="be504-109">EXAMPLES</span></span>

### <span data-ttu-id="be504-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="be504-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="be504-111">此命令會針對資料共用帳戶 WikiAds 下的共用訂閱 AdsShareSubscription，提供所有同步處理執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="be504-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="be504-112">參數</span><span class="sxs-lookup"><span data-stu-id="be504-112">PARAMETERS</span></span>

### <span data-ttu-id="be504-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="be504-113">-AccountName</span></span>
<span data-ttu-id="be504-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="be504-114">Azure data share account name</span></span>

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

### <span data-ttu-id="be504-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be504-115">-DefaultProfile</span></span>
<span data-ttu-id="be504-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="be504-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be504-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be504-117">-ResourceGroupName</span></span>
<span data-ttu-id="be504-118">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="be504-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="be504-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be504-119">-ResourceId</span></span>
<span data-ttu-id="be504-120">Azure 資料共用訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="be504-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="be504-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="be504-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="be504-122">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="be504-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="be504-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be504-123">CommonParameters</span></span>
<span data-ttu-id="be504-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="be504-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be504-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be504-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be504-126">輸入</span><span class="sxs-lookup"><span data-stu-id="be504-126">INPUTS</span></span>

### <span data-ttu-id="be504-127">System.String</span><span class="sxs-lookup"><span data-stu-id="be504-127">System.String</span></span>

## <span data-ttu-id="be504-128">輸出</span><span class="sxs-lookup"><span data-stu-id="be504-128">OUTPUTS</span></span>

### <span data-ttu-id="be504-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDShareSubscriptionSynchrononization</span><span class="sxs-lookup"><span data-stu-id="be504-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="be504-130">筆記</span><span class="sxs-lookup"><span data-stu-id="be504-130">NOTES</span></span>

## <span data-ttu-id="be504-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="be504-131">RELATED LINKS</span></span>
