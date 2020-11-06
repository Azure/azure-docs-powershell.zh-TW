---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 368423076003b03524272977ff8721db57721232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449325"
---
# <span data-ttu-id="a2085-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a2085-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="a2085-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2085-102">SYNOPSIS</span></span>
<span data-ttu-id="a2085-103">取得存取與媒體服務相關聯之 REST 端點的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="a2085-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2085-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2085-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2085-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2085-105">DESCRIPTION</span></span>
<span data-ttu-id="a2085-106">**AzureRmMediaServiceKeys** Cmdlet 會取得存取 Representational 狀態轉移 (REST 與 Azure 媒體服務相關聯的) 端點的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="a2085-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="a2085-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2085-107">EXAMPLES</span></span>

### <span data-ttu-id="a2085-108">範例1：取得存取媒體服務的重要資訊</span><span class="sxs-lookup"><span data-stu-id="a2085-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="a2085-109">這個命令會取得從屬於名為 ResourceGroup001 之資源群組的名為 MediaService001 的媒體服務的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="a2085-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="a2085-110">參數</span><span class="sxs-lookup"><span data-stu-id="a2085-110">PARAMETERS</span></span>

### <span data-ttu-id="a2085-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2085-111">-AccountName</span></span>
<span data-ttu-id="a2085-112">指定此 Cmdlet 取得媒體服務金鑰的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a2085-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2085-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2085-113">-DefaultProfile</span></span>
<span data-ttu-id="a2085-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a2085-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2085-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2085-115">-ResourceGroupName</span></span>
<span data-ttu-id="a2085-116">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2085-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2085-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2085-117">CommonParameters</span></span>
<span data-ttu-id="a2085-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2085-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2085-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2085-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2085-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a2085-120">INPUTS</span></span>

### <span data-ttu-id="a2085-121">所有</span><span class="sxs-lookup"><span data-stu-id="a2085-121">None</span></span>
<span data-ttu-id="a2085-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a2085-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2085-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a2085-123">OUTPUTS</span></span>

### <span data-ttu-id="a2085-124">PSServiceKeys 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2085-124">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="a2085-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a2085-125">NOTES</span></span>

## <span data-ttu-id="a2085-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2085-126">RELATED LINKS</span></span>

[<span data-ttu-id="a2085-127">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="a2085-127">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


