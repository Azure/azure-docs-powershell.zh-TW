---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273624"
---
# <span data-ttu-id="f4924-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="f4924-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="f4924-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4924-102">SYNOPSIS</span></span>
<span data-ttu-id="f4924-103">取得共用訂閱中觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4924-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="f4924-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4924-104">SYNTAX</span></span>

### <span data-ttu-id="f4924-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f4924-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4924-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4924-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4924-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4924-107">DESCRIPTION</span></span>
<span data-ttu-id="f4924-108">**AzDataShareTrigger** Cmdlet 會在 [資料共用帳戶] 下取得共用訂閱觸發程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4924-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="f4924-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4924-109">EXAMPLES</span></span>

### <span data-ttu-id="f4924-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f4924-110">Example 1</span></span>
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

<span data-ttu-id="f4924-111">這個命令會在 [資料共用帳戶 WikiAds] 下，取得共用訂閱 AdsShareSubscription 觸發程式 AdsTrigger 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4924-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="f4924-112">參數</span><span class="sxs-lookup"><span data-stu-id="f4924-112">PARAMETERS</span></span>

### <span data-ttu-id="f4924-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4924-113">-AccountName</span></span>
<span data-ttu-id="f4924-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="f4924-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f4924-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4924-115">-DefaultProfile</span></span>
<span data-ttu-id="f4924-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4924-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4924-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4924-117">-Name</span></span>
<span data-ttu-id="f4924-118">Azure 資料共用觸發程式名稱</span><span class="sxs-lookup"><span data-stu-id="f4924-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="f4924-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4924-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4924-120">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="f4924-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f4924-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4924-121">-ResourceId</span></span>
<span data-ttu-id="f4924-122">觸發程式的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f4924-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="f4924-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f4924-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="f4924-124">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="f4924-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="f4924-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4924-125">CommonParameters</span></span>
<span data-ttu-id="f4924-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4924-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4924-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4924-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4924-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f4924-128">INPUTS</span></span>

### <span data-ttu-id="f4924-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f4924-129">System.String</span></span>

## <span data-ttu-id="f4924-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f4924-130">OUTPUTS</span></span>

### <span data-ttu-id="f4924-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="f4924-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="f4924-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f4924-132">NOTES</span></span>

## <span data-ttu-id="f4924-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4924-133">RELATED LINKS</span></span>
