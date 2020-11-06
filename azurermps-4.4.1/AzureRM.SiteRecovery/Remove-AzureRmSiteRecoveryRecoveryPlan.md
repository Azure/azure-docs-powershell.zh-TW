---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449496"
---
# <span data-ttu-id="197c1-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="197c1-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="197c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="197c1-102">SYNOPSIS</span></span>
<span data-ttu-id="197c1-103">從網站復原中移除網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="197c1-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="197c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="197c1-104">SYNTAX</span></span>

### <span data-ttu-id="197c1-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="197c1-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="197c1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="197c1-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="197c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="197c1-107">DESCRIPTION</span></span>
<span data-ttu-id="197c1-108">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 會從目前的 Azure site recovery 中移除網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="197c1-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="197c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="197c1-109">EXAMPLES</span></span>

### <span data-ttu-id="197c1-110">範例1：移除恢復方案</span><span class="sxs-lookup"><span data-stu-id="197c1-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="197c1-111">第一個命令使用 Get-AzureRmSiteRecoveryRecoveryPlan Cmdlet 來取得網站復原方案，然後將它儲存在 $RecoveryPlan 變數中。</span><span class="sxs-lookup"><span data-stu-id="197c1-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="197c1-112">第二個命令會在 $RecoveryPlan 中移除復原方案。</span><span class="sxs-lookup"><span data-stu-id="197c1-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="197c1-113">參數</span><span class="sxs-lookup"><span data-stu-id="197c1-113">PARAMETERS</span></span>

### <span data-ttu-id="197c1-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="197c1-114">-Name</span></span>
<span data-ttu-id="197c1-115">指定此 Cmdlet 移除的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="197c1-115">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="197c1-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="197c1-116">-RecoveryPlan</span></span>
<span data-ttu-id="197c1-117">指定此 Cmdlet 移除的復原方案。</span><span class="sxs-lookup"><span data-stu-id="197c1-117">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="197c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="197c1-118">-DefaultProfile</span></span>
<span data-ttu-id="197c1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="197c1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="197c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="197c1-120">CommonParameters</span></span>
<span data-ttu-id="197c1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="197c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="197c1-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="197c1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="197c1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="197c1-123">INPUTS</span></span>

### <span data-ttu-id="197c1-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="197c1-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="197c1-125">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="197c1-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="197c1-126">輸出</span><span class="sxs-lookup"><span data-stu-id="197c1-126">OUTPUTS</span></span>

## <span data-ttu-id="197c1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="197c1-127">NOTES</span></span>

## <span data-ttu-id="197c1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="197c1-128">RELATED LINKS</span></span>

[<span data-ttu-id="197c1-129">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="197c1-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="197c1-130">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="197c1-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="197c1-131">更新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="197c1-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


