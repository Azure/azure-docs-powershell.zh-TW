---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: ae5a1d5a70064b3849bc8f38cab46ecfabaf4968
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625427"
---
# <span data-ttu-id="40f58-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40f58-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="40f58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40f58-102">SYNOPSIS</span></span>
<span data-ttu-id="40f58-103">在網站復原中取得復原計畫。</span><span class="sxs-lookup"><span data-stu-id="40f58-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40f58-104">句法</span><span class="sxs-lookup"><span data-stu-id="40f58-104">SYNTAX</span></span>

### <span data-ttu-id="40f58-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="40f58-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f58-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40f58-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f58-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="40f58-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40f58-108">說明</span><span class="sxs-lookup"><span data-stu-id="40f58-108">DESCRIPTION</span></span>
<span data-ttu-id="40f58-109">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 會在 Azure Site recovery 中取得恢復方案。</span><span class="sxs-lookup"><span data-stu-id="40f58-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="40f58-110">示例</span><span class="sxs-lookup"><span data-stu-id="40f58-110">EXAMPLES</span></span>

## <span data-ttu-id="40f58-111">參數</span><span class="sxs-lookup"><span data-stu-id="40f58-111">PARAMETERS</span></span>

### <span data-ttu-id="40f58-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f58-112">-DefaultProfile</span></span>
<span data-ttu-id="40f58-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40f58-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40f58-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="40f58-114">-FriendlyName</span></span>
<span data-ttu-id="40f58-115">指定此 Cmdlet 取得之復原方案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="40f58-115">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f58-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="40f58-116">-Name</span></span>
<span data-ttu-id="40f58-117">指定此 Cmdlet 取得的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="40f58-117">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="40f58-118">-Path</span><span class="sxs-lookup"><span data-stu-id="40f58-118">-Path</span></span>
<span data-ttu-id="40f58-119">指定此 Cmdlet 儲存恢復方案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="40f58-119">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f58-120">CommonParameters</span></span>
<span data-ttu-id="40f58-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40f58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f58-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40f58-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f58-123">輸入</span><span class="sxs-lookup"><span data-stu-id="40f58-123">INPUTS</span></span>

### <span data-ttu-id="40f58-124">所有</span><span class="sxs-lookup"><span data-stu-id="40f58-124">None</span></span>
<span data-ttu-id="40f58-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="40f58-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40f58-126">輸出</span><span class="sxs-lookup"><span data-stu-id="40f58-126">OUTPUTS</span></span>

### <span data-ttu-id="40f58-127">System.object. IEnumerable ' 1 [SiteRecovery. ASRRecoveryPlan] （）</span><span class="sxs-lookup"><span data-stu-id="40f58-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="40f58-128">筆記</span><span class="sxs-lookup"><span data-stu-id="40f58-128">NOTES</span></span>

## <span data-ttu-id="40f58-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="40f58-129">RELATED LINKS</span></span>

[<span data-ttu-id="40f58-130">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40f58-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="40f58-131">移除-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40f58-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="40f58-132">更新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40f58-132">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
