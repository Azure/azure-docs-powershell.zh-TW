---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 443abbab086fe08ac0a667776a07c792115aa5dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454836"
---
# <span data-ttu-id="5f35c-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5f35c-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="5f35c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f35c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f35c-103">取得網站恢復保護原則。</span><span class="sxs-lookup"><span data-stu-id="5f35c-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f35c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f35c-104">SYNTAX</span></span>

### <span data-ttu-id="5f35c-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="5f35c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f35c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5f35c-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f35c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f35c-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f35c-108">說明</span><span class="sxs-lookup"><span data-stu-id="5f35c-108">DESCRIPTION</span></span>
<span data-ttu-id="5f35c-109">AzureRmSiteRecoveryPolicy Cmdlet 會透過名稱 **取得** 已設定之 Azure 網站復原保護原則或特定保護原則的清單。</span><span class="sxs-lookup"><span data-stu-id="5f35c-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="5f35c-110">示例</span><span class="sxs-lookup"><span data-stu-id="5f35c-110">EXAMPLES</span></span>

## <span data-ttu-id="5f35c-111">參數</span><span class="sxs-lookup"><span data-stu-id="5f35c-111">PARAMETERS</span></span>

### <span data-ttu-id="5f35c-112">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f35c-112">-FriendlyName</span></span>
<span data-ttu-id="5f35c-113">指定網站復原複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5f35c-113">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="5f35c-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f35c-114">-Name</span></span>
<span data-ttu-id="5f35c-115">指定網站復原複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f35c-115">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="5f35c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f35c-116">-DefaultProfile</span></span>
<span data-ttu-id="5f35c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f35c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f35c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f35c-118">CommonParameters</span></span>
<span data-ttu-id="5f35c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f35c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f35c-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f35c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f35c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5f35c-121">INPUTS</span></span>

## <span data-ttu-id="5f35c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5f35c-122">OUTPUTS</span></span>

### <span data-ttu-id="5f35c-123">System.object. IEnumerable ' 1 [SiteRecovery. ASRPolicy] （）</span><span class="sxs-lookup"><span data-stu-id="5f35c-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="5f35c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5f35c-124">NOTES</span></span>

## <span data-ttu-id="5f35c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f35c-125">RELATED LINKS</span></span>

[<span data-ttu-id="5f35c-126">新-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5f35c-126">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="5f35c-127">移除-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5f35c-127">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
