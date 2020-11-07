---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: 6845e9db485133faf67e9a82875b199b6dd77dcf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786841"
---
# <span data-ttu-id="6279c-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="6279c-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="6279c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6279c-102">SYNOPSIS</span></span>
<span data-ttu-id="6279c-103">取得存取與媒體服務相關聯之 REST 端點的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="6279c-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="6279c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6279c-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6279c-105">說明</span><span class="sxs-lookup"><span data-stu-id="6279c-105">DESCRIPTION</span></span>
<span data-ttu-id="6279c-106">**AzMediaServiceKey** Cmdlet 會取得存取 Representational 狀態轉移 (REST 與 Azure 媒體服務相關聯的) 端點的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="6279c-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="6279c-107">示例</span><span class="sxs-lookup"><span data-stu-id="6279c-107">EXAMPLES</span></span>

### <span data-ttu-id="6279c-108">範例1：取得存取媒體服務的重要資訊</span><span class="sxs-lookup"><span data-stu-id="6279c-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="6279c-109">這個命令會取得從屬於名為 ResourceGroup001 之資源群組的名為 MediaService001 的媒體服務的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="6279c-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="6279c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6279c-110">PARAMETERS</span></span>

### <span data-ttu-id="6279c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6279c-111">-AccountName</span></span>
<span data-ttu-id="6279c-112">指定此 Cmdlet 取得媒體服務金鑰的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="6279c-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="6279c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6279c-113">-DefaultProfile</span></span>
<span data-ttu-id="6279c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6279c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6279c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6279c-115">-ResourceGroupName</span></span>
<span data-ttu-id="6279c-116">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6279c-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="6279c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6279c-117">CommonParameters</span></span>
<span data-ttu-id="6279c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6279c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6279c-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6279c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6279c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="6279c-120">INPUTS</span></span>

### <span data-ttu-id="6279c-121">System.object</span><span class="sxs-lookup"><span data-stu-id="6279c-121">System.String</span></span>

## <span data-ttu-id="6279c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6279c-122">OUTPUTS</span></span>

### <span data-ttu-id="6279c-123">PSServiceKeys 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6279c-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="6279c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6279c-124">NOTES</span></span>

## <span data-ttu-id="6279c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6279c-125">RELATED LINKS</span></span>

[<span data-ttu-id="6279c-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="6279c-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


