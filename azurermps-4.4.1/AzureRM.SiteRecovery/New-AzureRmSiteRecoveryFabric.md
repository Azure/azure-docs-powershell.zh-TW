---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625957"
---
# <span data-ttu-id="61360-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="61360-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="61360-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61360-102">SYNOPSIS</span></span>
<span data-ttu-id="61360-103">建立 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="61360-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61360-104">句法</span><span class="sxs-lookup"><span data-stu-id="61360-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61360-105">說明</span><span class="sxs-lookup"><span data-stu-id="61360-105">DESCRIPTION</span></span>
<span data-ttu-id="61360-106">**新的-AzureRmSiteRecoveryFabric** Cmdlet 會建立指定類型的 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="61360-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="61360-107">示例</span><span class="sxs-lookup"><span data-stu-id="61360-107">EXAMPLES</span></span>

## <span data-ttu-id="61360-108">參數</span><span class="sxs-lookup"><span data-stu-id="61360-108">PARAMETERS</span></span>

### <span data-ttu-id="61360-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="61360-109">-Name</span></span>
<span data-ttu-id="61360-110">指定 Azure 網站復原結構的名稱</span><span class="sxs-lookup"><span data-stu-id="61360-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61360-111">-類型</span><span class="sxs-lookup"><span data-stu-id="61360-111">-Type</span></span>
<span data-ttu-id="61360-112">指定 Azure Site Recovery 結構類型。</span><span class="sxs-lookup"><span data-stu-id="61360-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61360-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61360-113">-DefaultProfile</span></span>
<span data-ttu-id="61360-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61360-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61360-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61360-115">CommonParameters</span></span>
<span data-ttu-id="61360-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61360-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61360-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61360-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61360-118">輸入</span><span class="sxs-lookup"><span data-stu-id="61360-118">INPUTS</span></span>

## <span data-ttu-id="61360-119">輸出</span><span class="sxs-lookup"><span data-stu-id="61360-119">OUTPUTS</span></span>

### <span data-ttu-id="61360-120">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="61360-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="61360-121">筆記</span><span class="sxs-lookup"><span data-stu-id="61360-121">NOTES</span></span>

## <span data-ttu-id="61360-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="61360-122">RELATED LINKS</span></span>

[<span data-ttu-id="61360-123">AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="61360-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="61360-124">移除-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="61360-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
