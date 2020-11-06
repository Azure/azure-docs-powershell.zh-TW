---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454903"
---
# <span data-ttu-id="0e368-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0e368-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="0e368-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e368-102">SYNOPSIS</span></span>
<span data-ttu-id="0e368-103">取得 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0e368-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e368-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e368-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e368-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e368-105">DESCRIPTION</span></span>
<span data-ttu-id="0e368-106">**AzureRMCdnProfile** Cmdlet 會 (CDN) 設定檔及其相關資訊，取得 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="0e368-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="0e368-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e368-107">EXAMPLES</span></span>

## <span data-ttu-id="0e368-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e368-108">PARAMETERS</span></span>

### <span data-ttu-id="0e368-109">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0e368-109">-ProfileName</span></span>
<span data-ttu-id="0e368-110">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e368-110">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0e368-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e368-111">-ResourceGroupName</span></span>
<span data-ttu-id="0e368-112">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e368-112">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0e368-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e368-113">-DefaultProfile</span></span>
<span data-ttu-id="0e368-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e368-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e368-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e368-115">CommonParameters</span></span>
<span data-ttu-id="0e368-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e368-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e368-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e368-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e368-118">輸入</span><span class="sxs-lookup"><span data-stu-id="0e368-118">INPUTS</span></span>

## <span data-ttu-id="0e368-119">輸出</span><span class="sxs-lookup"><span data-stu-id="0e368-119">OUTPUTS</span></span>

###  
<span data-ttu-id="0e368-120">這個 Cmdlet 會傳回設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="0e368-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="0e368-121">筆記</span><span class="sxs-lookup"><span data-stu-id="0e368-121">NOTES</span></span>

## <span data-ttu-id="0e368-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e368-122">RELATED LINKS</span></span>

[<span data-ttu-id="0e368-123">新-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0e368-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="0e368-124">移除-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0e368-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="0e368-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0e368-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


