---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913541"
---
# <span data-ttu-id="2974c-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="2974c-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="2974c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2974c-102">SYNOPSIS</span></span>
<span data-ttu-id="2974c-103">建立新共用訂閱。</span><span class="sxs-lookup"><span data-stu-id="2974c-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="2974c-104">語法</span><span class="sxs-lookup"><span data-stu-id="2974c-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2974c-105">描述</span><span class="sxs-lookup"><span data-stu-id="2974c-105">DESCRIPTION</span></span>
<span data-ttu-id="2974c-106">**New-AzDataShareSubscription** Cmdlet 會以指定的資料共用帳戶和邀請識別碼建立共用訂閱。</span><span class="sxs-lookup"><span data-stu-id="2974c-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="2974c-107">例子</span><span class="sxs-lookup"><span data-stu-id="2974c-107">EXAMPLES</span></span>

### <span data-ttu-id="2974c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2974c-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="2974c-109">這個命令會針對資料共用帳戶 WikiAds 下的 invitaionId 建立新的共用訂閱 AdsShareSubscription。</span><span class="sxs-lookup"><span data-stu-id="2974c-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="2974c-110">參數</span><span class="sxs-lookup"><span data-stu-id="2974c-110">PARAMETERS</span></span>

### <span data-ttu-id="2974c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2974c-111">-AccountName</span></span>
<span data-ttu-id="2974c-112">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="2974c-112">Azure data share account name</span></span>

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

### <span data-ttu-id="2974c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2974c-113">-DefaultProfile</span></span>
<span data-ttu-id="2974c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2974c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2974c-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="2974c-115">-InvitationId</span></span>
<span data-ttu-id="2974c-116">Azure 資料共用邀請Id</span><span class="sxs-lookup"><span data-stu-id="2974c-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="2974c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2974c-117">-Name</span></span>
<span data-ttu-id="2974c-118">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="2974c-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2974c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2974c-119">-ResourceGroupName</span></span>
<span data-ttu-id="2974c-120">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="2974c-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2974c-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="2974c-121">-SourceShareLocation</span></span>
<span data-ttu-id="2974c-122">Azure 資料共用位置</span><span class="sxs-lookup"><span data-stu-id="2974c-122">Azure data share location</span></span>

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

### <span data-ttu-id="2974c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2974c-123">-Confirm</span></span>
<span data-ttu-id="2974c-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2974c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2974c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2974c-125">-WhatIf</span></span>
<span data-ttu-id="2974c-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2974c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2974c-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2974c-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2974c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2974c-128">CommonParameters</span></span>
<span data-ttu-id="2974c-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2974c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2974c-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2974c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2974c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2974c-131">INPUTS</span></span>

### <span data-ttu-id="2974c-132">沒有</span><span class="sxs-lookup"><span data-stu-id="2974c-132">None</span></span>

## <span data-ttu-id="2974c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2974c-133">OUTPUTS</span></span>

### <span data-ttu-id="2974c-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2974c-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2974c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2974c-135">NOTES</span></span>

## <span data-ttu-id="2974c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2974c-136">RELATED LINKS</span></span>
