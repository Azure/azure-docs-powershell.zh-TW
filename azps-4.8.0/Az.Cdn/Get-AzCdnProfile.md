---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969608"
---
# <span data-ttu-id="e3873-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e3873-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="e3873-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3873-102">SYNOPSIS</span></span>
<span data-ttu-id="e3873-103">取得 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3873-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="e3873-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3873-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3873-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3873-105">DESCRIPTION</span></span>
<span data-ttu-id="e3873-106">**AzCdnProfile** Cmdlet 會 (CDN) 設定檔及其相關資訊，取得 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="e3873-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="e3873-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3873-107">EXAMPLES</span></span>

## <span data-ttu-id="e3873-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3873-108">PARAMETERS</span></span>

### <span data-ttu-id="e3873-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3873-109">-DefaultProfile</span></span>
<span data-ttu-id="e3873-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e3873-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3873-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e3873-111">-ProfileName</span></span>
<span data-ttu-id="e3873-112">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3873-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e3873-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3873-113">-ResourceGroupName</span></span>
<span data-ttu-id="e3873-114">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3873-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e3873-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3873-115">CommonParameters</span></span>
<span data-ttu-id="e3873-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3873-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3873-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3873-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3873-118">輸入</span><span class="sxs-lookup"><span data-stu-id="e3873-118">INPUTS</span></span>

### <span data-ttu-id="e3873-119">System.object</span><span class="sxs-lookup"><span data-stu-id="e3873-119">System.String</span></span>

## <span data-ttu-id="e3873-120">輸出</span><span class="sxs-lookup"><span data-stu-id="e3873-120">OUTPUTS</span></span>

### <span data-ttu-id="e3873-121">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3873-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e3873-122">筆記</span><span class="sxs-lookup"><span data-stu-id="e3873-122">NOTES</span></span>

## <span data-ttu-id="e3873-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3873-123">RELATED LINKS</span></span>

[<span data-ttu-id="e3873-124">新-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e3873-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="e3873-125">移除-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e3873-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="e3873-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e3873-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)

