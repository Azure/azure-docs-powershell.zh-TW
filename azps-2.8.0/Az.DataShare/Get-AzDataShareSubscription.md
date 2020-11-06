---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 23553e939256b9124369afd79db29a50802dc6cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612673"
---
# <span data-ttu-id="28b0e-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="28b0e-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="28b0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="28b0e-103">取得資料共用帳戶中共用訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="28b0e-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="28b0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="28b0e-104">SYNTAX</span></span>

### <span data-ttu-id="28b0e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28b0e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28b0e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b0e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28b0e-107">說明</span><span class="sxs-lookup"><span data-stu-id="28b0e-107">DESCRIPTION</span></span>
<span data-ttu-id="28b0e-108">**AzDataShareSubscription** Cmdlet 提供有關在資料共用帳戶中共用訂閱的資訊。</span><span class="sxs-lookup"><span data-stu-id="28b0e-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="28b0e-109">如果提供共用訂閱名稱，則 Cmdlet 會提供特定共用訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="28b0e-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="28b0e-110">否則，此 Cmdlet 會在 [資料共用] 帳戶中提供共用訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="28b0e-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="28b0e-111">示例</span><span class="sxs-lookup"><span data-stu-id="28b0e-111">EXAMPLES</span></span>

### <span data-ttu-id="28b0e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="28b0e-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="28b0e-113">此命令會提供在資料共用帳戶 WikiAds 中共用訂閱 AdsShareSubscription 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="28b0e-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="28b0e-114">參數</span><span class="sxs-lookup"><span data-stu-id="28b0e-114">PARAMETERS</span></span>

### <span data-ttu-id="28b0e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28b0e-115">-AccountName</span></span>
<span data-ttu-id="28b0e-116">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="28b0e-116">Azure data share account name</span></span>

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

### <span data-ttu-id="28b0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b0e-117">-DefaultProfile</span></span>
<span data-ttu-id="28b0e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28b0e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b0e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="28b0e-119">-Name</span></span>
<span data-ttu-id="28b0e-120">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="28b0e-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="28b0e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b0e-121">-ResourceGroupName</span></span>
<span data-ttu-id="28b0e-122">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="28b0e-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="28b0e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b0e-123">-ResourceId</span></span>
<span data-ttu-id="28b0e-124">Azure 資料共用訂閱的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="28b0e-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="28b0e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b0e-125">CommonParameters</span></span>
<span data-ttu-id="28b0e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28b0e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b0e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28b0e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b0e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="28b0e-128">INPUTS</span></span>

### <span data-ttu-id="28b0e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="28b0e-129">System.String</span></span>

## <span data-ttu-id="28b0e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="28b0e-130">OUTPUTS</span></span>

### <span data-ttu-id="28b0e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="28b0e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="28b0e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="28b0e-132">NOTES</span></span>

## <span data-ttu-id="28b0e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="28b0e-133">RELATED LINKS</span></span>