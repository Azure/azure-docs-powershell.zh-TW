---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959627"
---
# <span data-ttu-id="79437-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79437-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="79437-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79437-102">SYNOPSIS</span></span>
<span data-ttu-id="79437-103">取得 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="79437-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="79437-104">句法</span><span class="sxs-lookup"><span data-stu-id="79437-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79437-105">說明</span><span class="sxs-lookup"><span data-stu-id="79437-105">DESCRIPTION</span></span>
<span data-ttu-id="79437-106">**AzCdnProfile** Cmdlet 會 (CDN) 設定檔及其相關資訊，取得 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="79437-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="79437-107">示例</span><span class="sxs-lookup"><span data-stu-id="79437-107">EXAMPLES</span></span>

## <span data-ttu-id="79437-108">參數</span><span class="sxs-lookup"><span data-stu-id="79437-108">PARAMETERS</span></span>

### <span data-ttu-id="79437-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79437-109">-DefaultProfile</span></span>
<span data-ttu-id="79437-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="79437-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79437-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="79437-111">-ProfileName</span></span>
<span data-ttu-id="79437-112">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="79437-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="79437-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79437-113">-ResourceGroupName</span></span>
<span data-ttu-id="79437-114">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79437-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="79437-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79437-115">CommonParameters</span></span>
<span data-ttu-id="79437-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79437-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79437-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79437-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79437-118">輸入</span><span class="sxs-lookup"><span data-stu-id="79437-118">INPUTS</span></span>

### <span data-ttu-id="79437-119">System.object</span><span class="sxs-lookup"><span data-stu-id="79437-119">System.String</span></span>

## <span data-ttu-id="79437-120">輸出</span><span class="sxs-lookup"><span data-stu-id="79437-120">OUTPUTS</span></span>

### <span data-ttu-id="79437-121">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="79437-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="79437-122">筆記</span><span class="sxs-lookup"><span data-stu-id="79437-122">NOTES</span></span>

## <span data-ttu-id="79437-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="79437-123">RELATED LINKS</span></span>

[<span data-ttu-id="79437-124">新-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79437-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="79437-125">移除-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79437-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="79437-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="79437-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)

