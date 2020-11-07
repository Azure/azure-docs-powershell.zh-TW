---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957111"
---
# <span data-ttu-id="d291d-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="d291d-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="d291d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d291d-102">SYNOPSIS</span></span>
<span data-ttu-id="d291d-103">取得消費者邀請的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d291d-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="d291d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d291d-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d291d-105">說明</span><span class="sxs-lookup"><span data-stu-id="d291d-105">DESCRIPTION</span></span>
<span data-ttu-id="d291d-106">**AzDataShareReceivedInvitation** Cmdlet 會提供有關消費者已 receieved 之所有邀請的資訊。</span><span class="sxs-lookup"><span data-stu-id="d291d-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="d291d-107">如果您提供位置或邀請 id，此 Cmdlet 會提供有關特定位置或具有邀請 id 的邀請資訊。否則，它會提供傳送給消費者的邀請清單。</span><span class="sxs-lookup"><span data-stu-id="d291d-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="d291d-108">示例</span><span class="sxs-lookup"><span data-stu-id="d291d-108">EXAMPLES</span></span>

### <span data-ttu-id="d291d-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d291d-109">Example 1</span></span>
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

<span data-ttu-id="d291d-110">此 commant 提供消費者邀請的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d291d-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="d291d-111">參數</span><span class="sxs-lookup"><span data-stu-id="d291d-111">PARAMETERS</span></span>

### <span data-ttu-id="d291d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d291d-112">-DefaultProfile</span></span>
<span data-ttu-id="d291d-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d291d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d291d-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="d291d-114">-InvitationId</span></span>
<span data-ttu-id="d291d-115">Azure dataShare 邀請 id。</span><span class="sxs-lookup"><span data-stu-id="d291d-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="d291d-116">-位置</span><span class="sxs-lookup"><span data-stu-id="d291d-116">-Location</span></span>
<span data-ttu-id="d291d-117">Azure 資料共用邀請位置。</span><span class="sxs-lookup"><span data-stu-id="d291d-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="d291d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d291d-118">CommonParameters</span></span>
<span data-ttu-id="d291d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d291d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d291d-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d291d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d291d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d291d-121">INPUTS</span></span>

### <span data-ttu-id="d291d-122">所有</span><span class="sxs-lookup"><span data-stu-id="d291d-122">None</span></span>

## <span data-ttu-id="d291d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d291d-123">OUTPUTS</span></span>

### <span data-ttu-id="d291d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d291d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d291d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d291d-125">NOTES</span></span>

## <span data-ttu-id="d291d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d291d-126">RELATED LINKS</span></span>
