---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 563c97ec87a758668c737465ea50642324706a9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916977"
---
# <span data-ttu-id="adc5d-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="adc5d-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="adc5d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="adc5d-103">獲得消費者邀請相關資訊。</span><span class="sxs-lookup"><span data-stu-id="adc5d-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="adc5d-104">語法</span><span class="sxs-lookup"><span data-stu-id="adc5d-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc5d-105">描述</span><span class="sxs-lookup"><span data-stu-id="adc5d-105">DESCRIPTION</span></span>
<span data-ttu-id="adc5d-106">**Get-AzDataShareReceivedInvitation Cmdlet** 會提供消費者已接受之所有邀請的資訊。</span><span class="sxs-lookup"><span data-stu-id="adc5d-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="adc5d-107">如果您提供位置或邀請識別碼，此 Cmdlet 會提供特定位置邀請或具有邀請識別碼的資訊。否則，它會提供一份寄給消費者的邀請清單。</span><span class="sxs-lookup"><span data-stu-id="adc5d-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="adc5d-108">例子</span><span class="sxs-lookup"><span data-stu-id="adc5d-108">EXAMPLES</span></span>

### <span data-ttu-id="adc5d-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="adc5d-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="adc5d-110">此企業會提供消費者邀請相關資訊。</span><span class="sxs-lookup"><span data-stu-id="adc5d-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="adc5d-111">參數</span><span class="sxs-lookup"><span data-stu-id="adc5d-111">PARAMETERS</span></span>

### <span data-ttu-id="adc5d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc5d-112">-DefaultProfile</span></span>
<span data-ttu-id="adc5d-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="adc5d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc5d-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="adc5d-114">-InvitationId</span></span>
<span data-ttu-id="adc5d-115">Azure DataShare 邀請識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc5d-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="adc5d-116">-位置</span><span class="sxs-lookup"><span data-stu-id="adc5d-116">-Location</span></span>
<span data-ttu-id="adc5d-117">Azure 資料共用邀請位置。</span><span class="sxs-lookup"><span data-stu-id="adc5d-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="adc5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc5d-118">CommonParameters</span></span>
<span data-ttu-id="adc5d-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adc5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc5d-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adc5d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc5d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="adc5d-121">INPUTS</span></span>

### <span data-ttu-id="adc5d-122">沒有</span><span class="sxs-lookup"><span data-stu-id="adc5d-122">None</span></span>

## <span data-ttu-id="adc5d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="adc5d-123">OUTPUTS</span></span>

### <span data-ttu-id="adc5d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="adc5d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="adc5d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="adc5d-125">NOTES</span></span>

## <span data-ttu-id="adc5d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="adc5d-126">RELATED LINKS</span></span>
