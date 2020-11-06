---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447962"
---
# <span data-ttu-id="a8dc2-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a8dc2-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="a8dc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a8dc2-103">取得 Azure Site Recovery 結構的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8dc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8dc2-104">SYNTAX</span></span>

### <span data-ttu-id="a8dc2-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a8dc2-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8dc2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a8dc2-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8dc2-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a8dc2-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8dc2-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="a8dc2-109">**AzureRmSiteRecoveryFabric** Cmdlet 會取得指定 Azure 網站復原結構的屬性，或在恢復服務電子倉庫中的所有 azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="a8dc2-110">示例</span><span class="sxs-lookup"><span data-stu-id="a8dc2-110">EXAMPLES</span></span>

## <span data-ttu-id="a8dc2-111">參數</span><span class="sxs-lookup"><span data-stu-id="a8dc2-111">PARAMETERS</span></span>

### <span data-ttu-id="a8dc2-112">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a8dc2-112">-FriendlyName</span></span>
<span data-ttu-id="a8dc2-113">指定 Azure 網站復原結構的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dc2-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8dc2-114">-Name</span></span>
<span data-ttu-id="a8dc2-115">指定 Azure 網站復原結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="a8dc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8dc2-116">-DefaultProfile</span></span>
<span data-ttu-id="a8dc2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8dc2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dc2-118">CommonParameters</span></span>
<span data-ttu-id="a8dc2-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dc2-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8dc2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dc2-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a8dc2-121">INPUTS</span></span>

## <span data-ttu-id="a8dc2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a8dc2-122">OUTPUTS</span></span>

### <span data-ttu-id="a8dc2-123">[System.object]。清單 ' 1 [SiteRecovery. ASRFabric，SiteRecovery，版本 = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （通用）</span><span class="sxs-lookup"><span data-stu-id="a8dc2-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a8dc2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a8dc2-124">NOTES</span></span>

## <span data-ttu-id="a8dc2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8dc2-125">RELATED LINKS</span></span>

[<span data-ttu-id="a8dc2-126">新-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a8dc2-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="a8dc2-127">移除-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a8dc2-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
