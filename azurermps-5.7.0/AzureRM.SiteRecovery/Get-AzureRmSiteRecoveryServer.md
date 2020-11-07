---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625425"
---
# <span data-ttu-id="933c7-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="933c7-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="933c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="933c7-102">SYNOPSIS</span></span>
<span data-ttu-id="933c7-103">取得已登錄至目前電子倉庫之網站復原伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="933c7-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="933c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="933c7-104">SYNTAX</span></span>

### <span data-ttu-id="933c7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="933c7-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933c7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="933c7-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933c7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="933c7-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="933c7-108">說明</span><span class="sxs-lookup"><span data-stu-id="933c7-108">DESCRIPTION</span></span>
<span data-ttu-id="933c7-109">**AzureRmSiteRecoveryServer** Cmdlet 會取得已登錄至目前網站復原電子倉庫之 Azure 網站復原伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="933c7-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="933c7-110">示例</span><span class="sxs-lookup"><span data-stu-id="933c7-110">EXAMPLES</span></span>

## <span data-ttu-id="933c7-111">參數</span><span class="sxs-lookup"><span data-stu-id="933c7-111">PARAMETERS</span></span>

### <span data-ttu-id="933c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933c7-112">-DefaultProfile</span></span>
<span data-ttu-id="933c7-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="933c7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="933c7-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="933c7-114">-FriendlyName</span></span>
<span data-ttu-id="933c7-115">指定伺服器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="933c7-115">Specifies the friendly name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="933c7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="933c7-116">-Name</span></span>
<span data-ttu-id="933c7-117">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="933c7-117">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="933c7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933c7-118">CommonParameters</span></span>
<span data-ttu-id="933c7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="933c7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933c7-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="933c7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933c7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="933c7-121">INPUTS</span></span>

### <span data-ttu-id="933c7-122">所有</span><span class="sxs-lookup"><span data-stu-id="933c7-122">None</span></span>
<span data-ttu-id="933c7-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="933c7-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="933c7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="933c7-124">OUTPUTS</span></span>

### <span data-ttu-id="933c7-125">System.object. IEnumerable ' 1 [SiteRecovery. ASRServer] （）</span><span class="sxs-lookup"><span data-stu-id="933c7-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="933c7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="933c7-126">NOTES</span></span>

## <span data-ttu-id="933c7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="933c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="933c7-128">移除-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="933c7-128">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
