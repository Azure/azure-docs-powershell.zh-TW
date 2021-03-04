---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: b28182a5593454b110b2fe4036b022a8d74c33d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916978"
---
# <span data-ttu-id="1f4ec-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1f4ec-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="1f4ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4ec-103">在提供者端獲得消費者共用訂閱相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="1f4ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f4ec-104">SYNTAX</span></span>

### <span data-ttu-id="1f4ec-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f4ec-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f4ec-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f4ec-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f4ec-107">描述</span><span class="sxs-lookup"><span data-stu-id="1f4ec-107">DESCRIPTION</span></span>
<span data-ttu-id="1f4ec-108">**Get-AzDataShareProviderSubscription** Cmdlet 會取得提供者端消費者共用訂閱的資訊。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="1f4ec-109">如果您指定共用子訂閱識別碼，此 Cmdlet 會獲得共用訂閱相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="1f4ec-110">如果您未指定共用訂閱識別碼，此 Cmdlet 會獲得與共享關聯的所有消費者共用訂閱相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="1f4ec-111">例子</span><span class="sxs-lookup"><span data-stu-id="1f4ec-111">EXAMPLES</span></span>

### <span data-ttu-id="1f4ec-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f4ec-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="1f4ec-113">這個命令提供與資料共用帳戶 WikiAds 中共用 AdsShare 相關聯的消費者共用訂閱相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="1f4ec-114">參數</span><span class="sxs-lookup"><span data-stu-id="1f4ec-114">PARAMETERS</span></span>

### <span data-ttu-id="1f4ec-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1f4ec-115">-AccountName</span></span>
<span data-ttu-id="1f4ec-116">Azure DataShare 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="1f4ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4ec-117">-DefaultProfile</span></span>
<span data-ttu-id="1f4ec-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f4ec-120">Azure DataShare 帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="1f4ec-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f4ec-121">-ResourceId</span></span>
<span data-ttu-id="1f4ec-122">共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1f4ec-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4ec-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1f4ec-123">-ShareName</span></span>
<span data-ttu-id="1f4ec-124">Azure DataShare 名稱。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="1f4ec-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f4ec-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="1f4ec-126">消費者共用訂閱的識別碼</span><span class="sxs-lookup"><span data-stu-id="1f4ec-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4ec-127">CommonParameters</span></span>
<span data-ttu-id="1f4ec-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f4ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4ec-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f4ec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4ec-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1f4ec-130">INPUTS</span></span>

### <span data-ttu-id="1f4ec-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1f4ec-131">System.String</span></span>

## <span data-ttu-id="1f4ec-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1f4ec-132">OUTPUTS</span></span>

### <span data-ttu-id="1f4ec-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1f4ec-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="1f4ec-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1f4ec-134">NOTES</span></span>

## <span data-ttu-id="1f4ec-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f4ec-135">RELATED LINKS</span></span>
