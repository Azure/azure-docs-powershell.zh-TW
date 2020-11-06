---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 64309b77801646e61e3a144bc4a7405e4e978aa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612645"
---
# <span data-ttu-id="83993-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="83993-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="83993-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83993-102">SYNOPSIS</span></span>
<span data-ttu-id="83993-103">建立新的共用訂閱。</span><span class="sxs-lookup"><span data-stu-id="83993-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="83993-104">句法</span><span class="sxs-lookup"><span data-stu-id="83993-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83993-105">說明</span><span class="sxs-lookup"><span data-stu-id="83993-105">DESCRIPTION</span></span>
<span data-ttu-id="83993-106">**新的-AzDataShareSubscription** Cmdlet 會在指定的資料共用帳戶和邀請 id 中建立共用訂閱。</span><span class="sxs-lookup"><span data-stu-id="83993-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="83993-107">示例</span><span class="sxs-lookup"><span data-stu-id="83993-107">EXAMPLES</span></span>

### <span data-ttu-id="83993-108">範例1</span><span class="sxs-lookup"><span data-stu-id="83993-108">Example 1</span></span>
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

<span data-ttu-id="83993-109">這個命令會在 [資料共用帳戶 WikiAds] 下為 invitaionId 建立新的共用訂閱 AdsShareSubscription。</span><span class="sxs-lookup"><span data-stu-id="83993-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="83993-110">參數</span><span class="sxs-lookup"><span data-stu-id="83993-110">PARAMETERS</span></span>

### <span data-ttu-id="83993-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="83993-111">-AccountName</span></span>
<span data-ttu-id="83993-112">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="83993-112">Azure data share account name</span></span>

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

### <span data-ttu-id="83993-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83993-113">-DefaultProfile</span></span>
<span data-ttu-id="83993-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83993-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83993-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="83993-115">-InvitationId</span></span>
<span data-ttu-id="83993-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="83993-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="83993-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="83993-117">-Name</span></span>
<span data-ttu-id="83993-118">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="83993-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="83993-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83993-119">-ResourceGroupName</span></span>
<span data-ttu-id="83993-120">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="83993-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="83993-121">-確認</span><span class="sxs-lookup"><span data-stu-id="83993-121">-Confirm</span></span>
<span data-ttu-id="83993-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83993-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83993-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83993-123">-WhatIf</span></span>
<span data-ttu-id="83993-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83993-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83993-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83993-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83993-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83993-126">CommonParameters</span></span>
<span data-ttu-id="83993-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83993-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83993-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83993-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83993-129">輸入</span><span class="sxs-lookup"><span data-stu-id="83993-129">INPUTS</span></span>

### <span data-ttu-id="83993-130">所有</span><span class="sxs-lookup"><span data-stu-id="83993-130">None</span></span>

## <span data-ttu-id="83993-131">輸出</span><span class="sxs-lookup"><span data-stu-id="83993-131">OUTPUTS</span></span>

### <span data-ttu-id="83993-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="83993-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="83993-133">筆記</span><span class="sxs-lookup"><span data-stu-id="83993-133">NOTES</span></span>

## <span data-ttu-id="83993-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="83993-134">RELATED LINKS</span></span>
