---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454680"
---
# <span data-ttu-id="021c5-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="021c5-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="021c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="021c5-102">SYNOPSIS</span></span>
<span data-ttu-id="021c5-103">取得 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="021c5-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="021c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="021c5-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="021c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="021c5-105">DESCRIPTION</span></span>
<span data-ttu-id="021c5-106">**AzureRMCdnProfile** Cmdlet 會 (CDN) 設定檔及其相關資訊，取得 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="021c5-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="021c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="021c5-107">EXAMPLES</span></span>

## <span data-ttu-id="021c5-108">參數</span><span class="sxs-lookup"><span data-stu-id="021c5-108">PARAMETERS</span></span>

### <span data-ttu-id="021c5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021c5-109">-DefaultProfile</span></span>
<span data-ttu-id="021c5-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="021c5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="021c5-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="021c5-111">-ProfileName</span></span>
<span data-ttu-id="021c5-112">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="021c5-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021c5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021c5-113">-ResourceGroupName</span></span>
<span data-ttu-id="021c5-114">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="021c5-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021c5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021c5-115">CommonParameters</span></span>
<span data-ttu-id="021c5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="021c5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021c5-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="021c5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021c5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="021c5-118">INPUTS</span></span>

### <span data-ttu-id="021c5-119">System.object</span><span class="sxs-lookup"><span data-stu-id="021c5-119">System.String</span></span>

## <span data-ttu-id="021c5-120">輸出</span><span class="sxs-lookup"><span data-stu-id="021c5-120">OUTPUTS</span></span>

### <span data-ttu-id="021c5-121">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="021c5-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="021c5-122">筆記</span><span class="sxs-lookup"><span data-stu-id="021c5-122">NOTES</span></span>

## <span data-ttu-id="021c5-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="021c5-123">RELATED LINKS</span></span>

[<span data-ttu-id="021c5-124">新-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="021c5-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="021c5-125">移除-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="021c5-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="021c5-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="021c5-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


