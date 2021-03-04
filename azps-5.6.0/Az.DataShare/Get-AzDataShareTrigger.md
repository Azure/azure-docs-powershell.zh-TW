---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 430f31a0e44f226584d06a341971ed206a2bf5d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916149"
---
# <span data-ttu-id="ef4b6-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="ef4b6-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="ef4b6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4b6-103">在共用訂閱中，獲得觸發者相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4b6-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="ef4b6-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef4b6-104">SYNTAX</span></span>

### <span data-ttu-id="ef4b6-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ef4b6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef4b6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef4b6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef4b6-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef4b6-107">DESCRIPTION</span></span>
<span data-ttu-id="ef4b6-108">**Get-AzDataShareTrigger Cmdlet** 會取得資料共用帳戶下共用訂閱觸發程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4b6-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="ef4b6-109">例子</span><span class="sxs-lookup"><span data-stu-id="ef4b6-109">EXAMPLES</span></span>

### <span data-ttu-id="ef4b6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef4b6-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="ef4b6-111">此命令會獲得觸發 AdsTrigger 以在資料共用帳戶 WikiAds 下觸發共用訂閱 AdsShareSubscription 的資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4b6-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="ef4b6-112">參數</span><span class="sxs-lookup"><span data-stu-id="ef4b6-112">PARAMETERS</span></span>

### <span data-ttu-id="ef4b6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef4b6-113">-AccountName</span></span>
<span data-ttu-id="ef4b6-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ef4b6-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ef4b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4b6-115">-DefaultProfile</span></span>
<span data-ttu-id="ef4b6-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef4b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4b6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef4b6-117">-Name</span></span>
<span data-ttu-id="ef4b6-118">Azure 資料共用觸發名稱</span><span class="sxs-lookup"><span data-stu-id="ef4b6-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef4b6-120">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="ef4b6-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ef4b6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef4b6-121">-ResourceId</span></span>
<span data-ttu-id="ef4b6-122">觸發者的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4b6-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="ef4b6-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ef4b6-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="ef4b6-124">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="ef4b6-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ef4b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4b6-125">CommonParameters</span></span>
<span data-ttu-id="ef4b6-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef4b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4b6-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef4b6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4b6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ef4b6-128">INPUTS</span></span>

### <span data-ttu-id="ef4b6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ef4b6-129">System.String</span></span>

## <span data-ttu-id="ef4b6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ef4b6-130">OUTPUTS</span></span>

### <span data-ttu-id="ef4b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="ef4b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="ef4b6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ef4b6-132">NOTES</span></span>

## <span data-ttu-id="ef4b6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef4b6-133">RELATED LINKS</span></span>
