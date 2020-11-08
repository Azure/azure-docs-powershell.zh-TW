---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140971"
---
# <span data-ttu-id="32e35-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="32e35-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="32e35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32e35-102">SYNOPSIS</span></span>
<span data-ttu-id="32e35-103">取得 CDN 設定檔的單一登入 URL。</span><span class="sxs-lookup"><span data-stu-id="32e35-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="32e35-104">句法</span><span class="sxs-lookup"><span data-stu-id="32e35-104">SYNTAX</span></span>

### <span data-ttu-id="32e35-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="32e35-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32e35-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32e35-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32e35-107">說明</span><span class="sxs-lookup"><span data-stu-id="32e35-107">DESCRIPTION</span></span>
<span data-ttu-id="32e35-108">**AzCdnProfileSsoUrl** Cmdlet 會取得 Azure 內容傳遞網路的單一登入 URL， (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="32e35-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="32e35-109">此 URL 可讓使用者連線至輔助入口網站，並使用 CDN 的其他功能。</span><span class="sxs-lookup"><span data-stu-id="32e35-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="32e35-110">示例</span><span class="sxs-lookup"><span data-stu-id="32e35-110">EXAMPLES</span></span>

## <span data-ttu-id="32e35-111">參數</span><span class="sxs-lookup"><span data-stu-id="32e35-111">PARAMETERS</span></span>

### <span data-ttu-id="32e35-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="32e35-112">-CdnProfile</span></span>
<span data-ttu-id="32e35-113">指定 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="32e35-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="32e35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e35-114">-DefaultProfile</span></span>
<span data-ttu-id="32e35-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="32e35-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32e35-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="32e35-116">-ProfileName</span></span>
<span data-ttu-id="32e35-117">指定 CDN 設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="32e35-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="32e35-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e35-118">-ResourceGroupName</span></span>
<span data-ttu-id="32e35-119">指定設定檔所屬之資源組名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="32e35-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="32e35-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e35-120">CommonParameters</span></span>
<span data-ttu-id="32e35-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32e35-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e35-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32e35-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e35-123">輸入</span><span class="sxs-lookup"><span data-stu-id="32e35-123">INPUTS</span></span>

### <span data-ttu-id="32e35-124">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32e35-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="32e35-125">輸出</span><span class="sxs-lookup"><span data-stu-id="32e35-125">OUTPUTS</span></span>

### <span data-ttu-id="32e35-126">PSSsoUri 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32e35-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="32e35-127">筆記</span><span class="sxs-lookup"><span data-stu-id="32e35-127">NOTES</span></span>

## <span data-ttu-id="32e35-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="32e35-128">RELATED LINKS</span></span>

[<span data-ttu-id="32e35-129">AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="32e35-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


