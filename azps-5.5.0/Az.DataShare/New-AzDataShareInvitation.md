---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138410"
---
# <span data-ttu-id="96ee1-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="96ee1-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="96ee1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="96ee1-103">建立共用邀請。</span><span class="sxs-lookup"><span data-stu-id="96ee1-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="96ee1-104">句法</span><span class="sxs-lookup"><span data-stu-id="96ee1-104">SYNTAX</span></span>

### <span data-ttu-id="96ee1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="96ee1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ee1-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="96ee1-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ee1-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="96ee1-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96ee1-108">說明</span><span class="sxs-lookup"><span data-stu-id="96ee1-108">DESCRIPTION</span></span>
<span data-ttu-id="96ee1-109">**新的 AzDataShareInvitation** Cmdlet 會傳送邀請給目標消費者，並提供提供者共用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96ee1-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="96ee1-110">示例</span><span class="sxs-lookup"><span data-stu-id="96ee1-110">EXAMPLES</span></span>

### <span data-ttu-id="96ee1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="96ee1-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="96ee1-112">這個命令會建立共用 AdsShare 的邀請 AdsInvitation，並將它傳送給目標電子郵件 adstest@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="96ee1-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="96ee1-113">參數</span><span class="sxs-lookup"><span data-stu-id="96ee1-113">PARAMETERS</span></span>

### <span data-ttu-id="96ee1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96ee1-114">-AccountName</span></span>
<span data-ttu-id="96ee1-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="96ee1-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ee1-116">-DefaultProfile</span></span>
<span data-ttu-id="96ee1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96ee1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96ee1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="96ee1-118">-Name</span></span>
<span data-ttu-id="96ee1-119">Azure 資料共用邀請名稱</span><span class="sxs-lookup"><span data-stu-id="96ee1-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ee1-120">-ResourceGroupName</span></span>
<span data-ttu-id="96ee1-121">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="96ee1-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-122">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="96ee1-122">-ShareName</span></span>
<span data-ttu-id="96ee1-123">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="96ee1-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="96ee1-124">-TargetEmail</span></span>
<span data-ttu-id="96ee1-125">目標電子郵件識別碼</span><span class="sxs-lookup"><span data-stu-id="96ee1-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="96ee1-126">-TargetObjectId</span></span>
<span data-ttu-id="96ee1-127">目標物件識別碼</span><span class="sxs-lookup"><span data-stu-id="96ee1-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="96ee1-128">-TargetTenantId</span></span>
<span data-ttu-id="96ee1-129">目標租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="96ee1-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ee1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="96ee1-130">-Confirm</span></span>
<span data-ttu-id="96ee1-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96ee1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96ee1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96ee1-132">-WhatIf</span></span>
<span data-ttu-id="96ee1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96ee1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96ee1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96ee1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96ee1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ee1-135">CommonParameters</span></span>
<span data-ttu-id="96ee1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96ee1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ee1-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96ee1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ee1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="96ee1-138">INPUTS</span></span>

### <span data-ttu-id="96ee1-139">所有</span><span class="sxs-lookup"><span data-stu-id="96ee1-139">None</span></span>

## <span data-ttu-id="96ee1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="96ee1-140">OUTPUTS</span></span>

### <span data-ttu-id="96ee1-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="96ee1-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="96ee1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="96ee1-142">NOTES</span></span>

## <span data-ttu-id="96ee1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="96ee1-143">RELATED LINKS</span></span>
