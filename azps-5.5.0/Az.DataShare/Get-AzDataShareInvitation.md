---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 0a723400bf92569a077abc64467c3cace56da0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141015"
---
# <span data-ttu-id="2b69a-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="2b69a-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="2b69a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b69a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b69a-103">取得資料共用的資訊邀請。</span><span class="sxs-lookup"><span data-stu-id="2b69a-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="2b69a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b69a-104">SYNTAX</span></span>

### <span data-ttu-id="2b69a-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2b69a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b69a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b69a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b69a-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b69a-107">DESCRIPTION</span></span>
<span data-ttu-id="2b69a-108">**AzDataShareInvitation** Cmdlet 會取得在資料共用中新增之邀請的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2b69a-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="2b69a-109">如果您指定邀請的名稱，此 Cmdlet 會取得邀請的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2b69a-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="2b69a-110">如果您沒有指定名稱，此 Cmdlet 會取得共用中所有邀請的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2b69a-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="2b69a-111">示例</span><span class="sxs-lookup"><span data-stu-id="2b69a-111">EXAMPLES</span></span>

### <span data-ttu-id="2b69a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="2b69a-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="2b69a-113">此命令會提供資料共用 AdsShare 中的邀請 AdsInvitation 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2b69a-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="2b69a-114">參數</span><span class="sxs-lookup"><span data-stu-id="2b69a-114">PARAMETERS</span></span>

### <span data-ttu-id="2b69a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b69a-115">-AccountName</span></span>
<span data-ttu-id="2b69a-116">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="2b69a-116">Azure data share account name</span></span>

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

### <span data-ttu-id="2b69a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b69a-117">-DefaultProfile</span></span>
<span data-ttu-id="2b69a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b69a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b69a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b69a-119">-Name</span></span>
<span data-ttu-id="2b69a-120">Azure 資料共用邀請名稱</span><span class="sxs-lookup"><span data-stu-id="2b69a-120">Azure data share invitation name</span></span>

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

### <span data-ttu-id="2b69a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b69a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b69a-122">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="2b69a-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2b69a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b69a-123">-ResourceId</span></span>
<span data-ttu-id="2b69a-124">Azure 資料共用邀請的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2b69a-124">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="2b69a-125">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="2b69a-125">-ShareName</span></span>
<span data-ttu-id="2b69a-126">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="2b69a-126">Azure data share name</span></span>

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

### <span data-ttu-id="2b69a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b69a-127">CommonParameters</span></span>
<span data-ttu-id="2b69a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b69a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b69a-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b69a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b69a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2b69a-130">INPUTS</span></span>

### <span data-ttu-id="2b69a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="2b69a-131">System.String</span></span>

## <span data-ttu-id="2b69a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2b69a-132">OUTPUTS</span></span>

### <span data-ttu-id="2b69a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2b69a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2b69a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2b69a-134">NOTES</span></span>

## <span data-ttu-id="2b69a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b69a-135">RELATED LINKS</span></span>
