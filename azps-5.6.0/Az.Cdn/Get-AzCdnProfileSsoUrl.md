---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904746"
---
# <span data-ttu-id="196e3-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="196e3-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="196e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="196e3-102">SYNOPSIS</span></span>
<span data-ttu-id="196e3-103">獲得 CDN 設定檔的單一登入 URL。</span><span class="sxs-lookup"><span data-stu-id="196e3-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="196e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="196e3-104">SYNTAX</span></span>

### <span data-ttu-id="196e3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="196e3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="196e3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="196e3-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="196e3-107">描述</span><span class="sxs-lookup"><span data-stu-id="196e3-107">DESCRIPTION</span></span>
<span data-ttu-id="196e3-108">**Get-AzCdnProfileSsoUrl** Cmdlet 會取得 Azure 內容傳遞網路 (CDN 設定檔) URL。</span><span class="sxs-lookup"><span data-stu-id="196e3-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="196e3-109">此 URL 可讓使用者連接至補充入口網站，並使用 CDN 的其他功能。</span><span class="sxs-lookup"><span data-stu-id="196e3-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="196e3-110">例子</span><span class="sxs-lookup"><span data-stu-id="196e3-110">EXAMPLES</span></span>

## <span data-ttu-id="196e3-111">參數</span><span class="sxs-lookup"><span data-stu-id="196e3-111">PARAMETERS</span></span>

### <span data-ttu-id="196e3-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="196e3-112">-CdnProfile</span></span>
<span data-ttu-id="196e3-113">指定 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="196e3-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="196e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196e3-114">-DefaultProfile</span></span>
<span data-ttu-id="196e3-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="196e3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e3-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="196e3-116">-ProfileName</span></span>
<span data-ttu-id="196e3-117">指定 CDN 設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="196e3-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="196e3-119">指定設定檔所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="196e3-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196e3-120">CommonParameters</span></span>
<span data-ttu-id="196e3-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="196e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196e3-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="196e3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196e3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="196e3-123">INPUTS</span></span>

### <span data-ttu-id="196e3-124">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="196e3-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="196e3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="196e3-125">OUTPUTS</span></span>

### <span data-ttu-id="196e3-126">Microsoft.Azure.Commands.Cdn.models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="196e3-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="196e3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="196e3-127">NOTES</span></span>

## <span data-ttu-id="196e3-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="196e3-128">RELATED LINKS</span></span>

[<span data-ttu-id="196e3-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="196e3-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


