---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625407"
---
# <span data-ttu-id="46795-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46795-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="46795-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46795-102">SYNOPSIS</span></span>
<span data-ttu-id="46795-103">從網站復原中移除網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="46795-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46795-104">句法</span><span class="sxs-lookup"><span data-stu-id="46795-104">SYNTAX</span></span>

### <span data-ttu-id="46795-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="46795-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46795-106">ByName</span><span class="sxs-lookup"><span data-stu-id="46795-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46795-107">說明</span><span class="sxs-lookup"><span data-stu-id="46795-107">DESCRIPTION</span></span>
<span data-ttu-id="46795-108">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 會從目前的 Azure site recovery 中移除網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="46795-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="46795-109">示例</span><span class="sxs-lookup"><span data-stu-id="46795-109">EXAMPLES</span></span>

### <span data-ttu-id="46795-110">範例1：移除恢復方案</span><span class="sxs-lookup"><span data-stu-id="46795-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="46795-111">第一個命令使用 Get-AzureRmSiteRecoveryRecoveryPlan Cmdlet 來取得網站復原方案，然後將它儲存在 $RecoveryPlan 變數中。</span><span class="sxs-lookup"><span data-stu-id="46795-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="46795-112">第二個命令會在 $RecoveryPlan 中移除復原方案。</span><span class="sxs-lookup"><span data-stu-id="46795-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="46795-113">參數</span><span class="sxs-lookup"><span data-stu-id="46795-113">PARAMETERS</span></span>

### <span data-ttu-id="46795-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46795-114">-DefaultProfile</span></span>
<span data-ttu-id="46795-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46795-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46795-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="46795-116">-Name</span></span>
<span data-ttu-id="46795-117">指定此 Cmdlet 移除的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="46795-117">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46795-118">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46795-118">-RecoveryPlan</span></span>
<span data-ttu-id="46795-119">指定此 Cmdlet 移除的復原方案。</span><span class="sxs-lookup"><span data-stu-id="46795-119">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46795-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46795-120">CommonParameters</span></span>
<span data-ttu-id="46795-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46795-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46795-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46795-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46795-123">輸入</span><span class="sxs-lookup"><span data-stu-id="46795-123">INPUTS</span></span>

### <span data-ttu-id="46795-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46795-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="46795-125">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="46795-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="46795-126">輸出</span><span class="sxs-lookup"><span data-stu-id="46795-126">OUTPUTS</span></span>

## <span data-ttu-id="46795-127">筆記</span><span class="sxs-lookup"><span data-stu-id="46795-127">NOTES</span></span>

## <span data-ttu-id="46795-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="46795-128">RELATED LINKS</span></span>

[<span data-ttu-id="46795-129">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46795-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="46795-130">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46795-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="46795-131">更新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46795-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


