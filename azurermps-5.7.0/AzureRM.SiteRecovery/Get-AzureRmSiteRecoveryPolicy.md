---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445984"
---
# <span data-ttu-id="cbdaa-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdaa-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="cbdaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbdaa-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdaa-103">取得網站恢復保護原則。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbdaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbdaa-104">SYNTAX</span></span>

### <span data-ttu-id="cbdaa-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="cbdaa-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbdaa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cbdaa-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbdaa-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cbdaa-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdaa-108">說明</span><span class="sxs-lookup"><span data-stu-id="cbdaa-108">DESCRIPTION</span></span>
<span data-ttu-id="cbdaa-109">AzureRmSiteRecoveryPolicy Cmdlet 會透過名稱 **取得** 已設定之 Azure 網站復原保護原則或特定保護原則的清單。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="cbdaa-110">示例</span><span class="sxs-lookup"><span data-stu-id="cbdaa-110">EXAMPLES</span></span>

## <span data-ttu-id="cbdaa-111">參數</span><span class="sxs-lookup"><span data-stu-id="cbdaa-111">PARAMETERS</span></span>

### <span data-ttu-id="cbdaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdaa-112">-DefaultProfile</span></span>
<span data-ttu-id="cbdaa-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbdaa-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cbdaa-114">-FriendlyName</span></span>
<span data-ttu-id="cbdaa-115">指定網站復原複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="cbdaa-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbdaa-116">-Name</span></span>
<span data-ttu-id="cbdaa-117">指定網站復原複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-117">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="cbdaa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdaa-118">CommonParameters</span></span>
<span data-ttu-id="cbdaa-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdaa-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdaa-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cbdaa-121">INPUTS</span></span>

### <span data-ttu-id="cbdaa-122">所有</span><span class="sxs-lookup"><span data-stu-id="cbdaa-122">None</span></span>
<span data-ttu-id="cbdaa-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cbdaa-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cbdaa-124">輸出</span><span class="sxs-lookup"><span data-stu-id="cbdaa-124">OUTPUTS</span></span>

### <span data-ttu-id="cbdaa-125">System.object. IEnumerable ' 1 [SiteRecovery. ASRPolicy] （）</span><span class="sxs-lookup"><span data-stu-id="cbdaa-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="cbdaa-126">筆記</span><span class="sxs-lookup"><span data-stu-id="cbdaa-126">NOTES</span></span>

## <span data-ttu-id="cbdaa-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbdaa-127">RELATED LINKS</span></span>

[<span data-ttu-id="cbdaa-128">新-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdaa-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="cbdaa-129">移除-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cbdaa-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
