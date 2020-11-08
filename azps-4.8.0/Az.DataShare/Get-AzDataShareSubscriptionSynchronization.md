---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136465"
---
# <span data-ttu-id="d9e73-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="d9e73-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="d9e73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9e73-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e73-103">取得在共用訂閱中執行同步處理的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d9e73-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="d9e73-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9e73-104">SYNTAX</span></span>

### <span data-ttu-id="d9e73-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d9e73-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9e73-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e73-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9e73-107">說明</span><span class="sxs-lookup"><span data-stu-id="d9e73-107">DESCRIPTION</span></span>
<span data-ttu-id="d9e73-108">**AzDataShareSubscriptionSynchronization** Cmdlet 在消費者的資料共用帳戶下，提供共用訂閱中的所有同步處理執行的 informaiton。</span><span class="sxs-lookup"><span data-stu-id="d9e73-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="d9e73-109">示例</span><span class="sxs-lookup"><span data-stu-id="d9e73-109">EXAMPLES</span></span>

### <span data-ttu-id="d9e73-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d9e73-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="d9e73-111">這個命令會在 [資料共用帳戶 WikiAds] 下，提供共用訂閱 AdsShareSubscription 的所有同步執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d9e73-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="d9e73-112">參數</span><span class="sxs-lookup"><span data-stu-id="d9e73-112">PARAMETERS</span></span>

### <span data-ttu-id="d9e73-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d9e73-113">-AccountName</span></span>
<span data-ttu-id="d9e73-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="d9e73-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d9e73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e73-115">-DefaultProfile</span></span>
<span data-ttu-id="d9e73-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9e73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9e73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e73-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9e73-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="d9e73-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d9e73-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9e73-119">-ResourceId</span></span>
<span data-ttu-id="d9e73-120">Azure 資料共用訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d9e73-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="d9e73-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d9e73-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="d9e73-122">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="d9e73-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d9e73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e73-123">CommonParameters</span></span>
<span data-ttu-id="d9e73-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9e73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e73-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9e73-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e73-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d9e73-126">INPUTS</span></span>

### <span data-ttu-id="d9e73-127">System.object</span><span class="sxs-lookup"><span data-stu-id="d9e73-127">System.String</span></span>

## <span data-ttu-id="d9e73-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d9e73-128">OUTPUTS</span></span>

### <span data-ttu-id="d9e73-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="d9e73-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="d9e73-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d9e73-130">NOTES</span></span>

## <span data-ttu-id="d9e73-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9e73-131">RELATED LINKS</span></span>
