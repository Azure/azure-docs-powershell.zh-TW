---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 2365502bb681cafe8ed7fedb05a4a862e54a3cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624850"
---
# <span data-ttu-id="c3814-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="c3814-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="c3814-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3814-102">SYNOPSIS</span></span>
<span data-ttu-id="c3814-103">取得 CDN 設定檔的單一登入 URL。</span><span class="sxs-lookup"><span data-stu-id="c3814-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3814-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3814-104">SYNTAX</span></span>

### <span data-ttu-id="c3814-105">預設)  (欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="c3814-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3814-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="c3814-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3814-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3814-107">DESCRIPTION</span></span>
<span data-ttu-id="c3814-108">**AzureRmCdnProfileSsoUrl** Cmdlet 會取得 Azure 內容傳遞網路的單一登入 URL， (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c3814-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="c3814-109">此 URL 可讓使用者 conntect 至輔助入口網站，並使用 CDN 的其他功能。</span><span class="sxs-lookup"><span data-stu-id="c3814-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="c3814-110">示例</span><span class="sxs-lookup"><span data-stu-id="c3814-110">EXAMPLES</span></span>

## <span data-ttu-id="c3814-111">參數</span><span class="sxs-lookup"><span data-stu-id="c3814-111">PARAMETERS</span></span>

### <span data-ttu-id="c3814-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c3814-112">-CdnProfile</span></span>
<span data-ttu-id="c3814-113">指定 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c3814-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3814-114">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c3814-114">-ProfileName</span></span>
<span data-ttu-id="c3814-115">指定 CDN 設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3814-115">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3814-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3814-116">-ResourceGroupName</span></span>
<span data-ttu-id="c3814-117">指定設定檔所屬之資源組名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3814-117">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3814-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3814-118">-DefaultProfile</span></span>
<span data-ttu-id="c3814-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3814-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3814-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3814-120">CommonParameters</span></span>
<span data-ttu-id="c3814-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3814-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3814-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3814-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3814-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c3814-123">INPUTS</span></span>

### <span data-ttu-id="c3814-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="c3814-124">PSProfile</span></span>
<span data-ttu-id="c3814-125">形參 "CdnProfile" 接受管線中 "PSProfile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c3814-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="c3814-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c3814-126">OUTPUTS</span></span>

###  
<span data-ttu-id="c3814-127">這個 Cmdlet 會傳回 URL。</span><span class="sxs-lookup"><span data-stu-id="c3814-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="c3814-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c3814-128">NOTES</span></span>

## <span data-ttu-id="c3814-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3814-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3814-130">AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c3814-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


