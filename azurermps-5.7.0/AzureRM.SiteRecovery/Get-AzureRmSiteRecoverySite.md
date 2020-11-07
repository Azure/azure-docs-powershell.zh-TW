---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625422"
---
# <span data-ttu-id="25f07-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="25f07-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="25f07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25f07-102">SYNOPSIS</span></span>
<span data-ttu-id="25f07-103">從 Site Recovery 保存庫取得 Hyper-v 網站。</span><span class="sxs-lookup"><span data-stu-id="25f07-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25f07-104">句法</span><span class="sxs-lookup"><span data-stu-id="25f07-104">SYNTAX</span></span>

### <span data-ttu-id="25f07-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="25f07-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f07-106">ByName</span><span class="sxs-lookup"><span data-stu-id="25f07-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25f07-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="25f07-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25f07-108">說明</span><span class="sxs-lookup"><span data-stu-id="25f07-108">DESCRIPTION</span></span>
<span data-ttu-id="25f07-109">**AzureRmSiteRecoverySite** Cmdlet 會取得 Azure Site Recovery 保存庫中的 hyper-v 網站。</span><span class="sxs-lookup"><span data-stu-id="25f07-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="25f07-110">示例</span><span class="sxs-lookup"><span data-stu-id="25f07-110">EXAMPLES</span></span>

## <span data-ttu-id="25f07-111">參數</span><span class="sxs-lookup"><span data-stu-id="25f07-111">PARAMETERS</span></span>

### <span data-ttu-id="25f07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f07-112">-DefaultProfile</span></span>
<span data-ttu-id="25f07-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25f07-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25f07-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="25f07-114">-FriendlyName</span></span>
<span data-ttu-id="25f07-115">指定網站的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="25f07-115">Specifies the friendly name of the site.</span></span>

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

### <span data-ttu-id="25f07-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="25f07-116">-Name</span></span>
<span data-ttu-id="25f07-117">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="25f07-117">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="25f07-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f07-118">CommonParameters</span></span>
<span data-ttu-id="25f07-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25f07-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f07-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25f07-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f07-121">輸入</span><span class="sxs-lookup"><span data-stu-id="25f07-121">INPUTS</span></span>

### <span data-ttu-id="25f07-122">所有</span><span class="sxs-lookup"><span data-stu-id="25f07-122">None</span></span>
<span data-ttu-id="25f07-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="25f07-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25f07-124">輸出</span><span class="sxs-lookup"><span data-stu-id="25f07-124">OUTPUTS</span></span>

### <span data-ttu-id="25f07-125">[System.object]. 清單 ' 1 [SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="25f07-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="25f07-126">筆記</span><span class="sxs-lookup"><span data-stu-id="25f07-126">NOTES</span></span>

## <span data-ttu-id="25f07-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="25f07-127">RELATED LINKS</span></span>

[<span data-ttu-id="25f07-128">新-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="25f07-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="25f07-129">移除-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="25f07-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
