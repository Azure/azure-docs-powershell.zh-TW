---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: e82e455d603ca4fd5d577e18337c93a2368fbcf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915606"
---
# <span data-ttu-id="91229-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="91229-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="91229-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91229-102">SYNOPSIS</span></span>
<span data-ttu-id="91229-103">獲得 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="91229-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="91229-104">語法</span><span class="sxs-lookup"><span data-stu-id="91229-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91229-105">描述</span><span class="sxs-lookup"><span data-stu-id="91229-105">DESCRIPTION</span></span>
<span data-ttu-id="91229-106">**Get-AzCdnProfile** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 設定檔及其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="91229-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="91229-107">例子</span><span class="sxs-lookup"><span data-stu-id="91229-107">EXAMPLES</span></span>

## <span data-ttu-id="91229-108">參數</span><span class="sxs-lookup"><span data-stu-id="91229-108">PARAMETERS</span></span>

### <span data-ttu-id="91229-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91229-109">-DefaultProfile</span></span>
<span data-ttu-id="91229-110">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="91229-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91229-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="91229-111">-ProfileName</span></span>
<span data-ttu-id="91229-112">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="91229-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="91229-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91229-113">-ResourceGroupName</span></span>
<span data-ttu-id="91229-114">指定設定檔所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="91229-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="91229-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91229-115">CommonParameters</span></span>
<span data-ttu-id="91229-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91229-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91229-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91229-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91229-118">輸入</span><span class="sxs-lookup"><span data-stu-id="91229-118">INPUTS</span></span>

### <span data-ttu-id="91229-119">System.String</span><span class="sxs-lookup"><span data-stu-id="91229-119">System.String</span></span>

## <span data-ttu-id="91229-120">輸出</span><span class="sxs-lookup"><span data-stu-id="91229-120">OUTPUTS</span></span>

### <span data-ttu-id="91229-121">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="91229-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="91229-122">筆記</span><span class="sxs-lookup"><span data-stu-id="91229-122">NOTES</span></span>

## <span data-ttu-id="91229-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="91229-123">RELATED LINKS</span></span>

[<span data-ttu-id="91229-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="91229-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="91229-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="91229-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="91229-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="91229-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


