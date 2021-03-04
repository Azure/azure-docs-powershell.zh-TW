---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: 59f288c74c8f5230375a475df839c491e07e58d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913514"
---
# <span data-ttu-id="8ab67-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8ab67-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="8ab67-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ab67-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab67-103">取得存取與媒體服務關聯的 REST 端點的金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="8ab67-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="8ab67-104">語法</span><span class="sxs-lookup"><span data-stu-id="8ab67-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab67-105">描述</span><span class="sxs-lookup"><span data-stu-id="8ab67-105">DESCRIPTION</span></span>
<span data-ttu-id="8ab67-106">**Get-AzMediaServiceKey** Cmdlet 會取得存取與 Azure 媒體服務關聯的表示狀態傳輸 (REST) 端點的金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="8ab67-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="8ab67-107">例子</span><span class="sxs-lookup"><span data-stu-id="8ab67-107">EXAMPLES</span></span>

### <span data-ttu-id="8ab67-108">範例 1：取得存取媒體服務的金鑰資訊</span><span class="sxs-lookup"><span data-stu-id="8ab67-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="8ab67-109">此命令會取得存取名為 MediaService001 的媒體服務之金鑰資訊，該服務屬於名為 ResourceGroup001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8ab67-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="8ab67-110">參數</span><span class="sxs-lookup"><span data-stu-id="8ab67-110">PARAMETERS</span></span>

### <span data-ttu-id="8ab67-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ab67-111">-AccountName</span></span>
<span data-ttu-id="8ab67-112">指定此 Cmdlet 從該 Cmdlet 獲得媒體服務金鑰的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8ab67-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab67-113">-DefaultProfile</span></span>
<span data-ttu-id="8ab67-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8ab67-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ab67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab67-115">-ResourceGroupName</span></span>
<span data-ttu-id="8ab67-116">指定包含媒體服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8ab67-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab67-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab67-117">CommonParameters</span></span>
<span data-ttu-id="8ab67-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ab67-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab67-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8ab67-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab67-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8ab67-120">INPUTS</span></span>

### <span data-ttu-id="8ab67-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8ab67-121">System.String</span></span>

## <span data-ttu-id="8ab67-122">輸出</span><span class="sxs-lookup"><span data-stu-id="8ab67-122">OUTPUTS</span></span>

### <span data-ttu-id="8ab67-123">Microsoft.Azure.Commands.Media.models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="8ab67-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="8ab67-124">筆記</span><span class="sxs-lookup"><span data-stu-id="8ab67-124">NOTES</span></span>

## <span data-ttu-id="8ab67-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ab67-125">RELATED LINKS</span></span>

[<span data-ttu-id="8ab67-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8ab67-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


