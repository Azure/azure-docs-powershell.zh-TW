---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446656"
---
# <span data-ttu-id="49489-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="49489-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="49489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49489-102">SYNOPSIS</span></span>
<span data-ttu-id="49489-103">建立網站恢復網站。</span><span class="sxs-lookup"><span data-stu-id="49489-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49489-104">句法</span><span class="sxs-lookup"><span data-stu-id="49489-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49489-105">說明</span><span class="sxs-lookup"><span data-stu-id="49489-105">DESCRIPTION</span></span>
<span data-ttu-id="49489-106">**新的 AzureRmSiteRecoverySite** Cmdlet 會在目前的電子倉庫中建立 Azure Site Recovery 網站。</span><span class="sxs-lookup"><span data-stu-id="49489-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="49489-107">示例</span><span class="sxs-lookup"><span data-stu-id="49489-107">EXAMPLES</span></span>

## <span data-ttu-id="49489-108">參數</span><span class="sxs-lookup"><span data-stu-id="49489-108">PARAMETERS</span></span>

### <span data-ttu-id="49489-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="49489-109">-Name</span></span>
<span data-ttu-id="49489-110">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="49489-110">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49489-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49489-111">-DefaultProfile</span></span>
<span data-ttu-id="49489-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49489-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49489-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49489-113">CommonParameters</span></span>
<span data-ttu-id="49489-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49489-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49489-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49489-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49489-116">輸入</span><span class="sxs-lookup"><span data-stu-id="49489-116">INPUTS</span></span>

## <span data-ttu-id="49489-117">輸出</span><span class="sxs-lookup"><span data-stu-id="49489-117">OUTPUTS</span></span>

## <span data-ttu-id="49489-118">筆記</span><span class="sxs-lookup"><span data-stu-id="49489-118">NOTES</span></span>

## <span data-ttu-id="49489-119">相關連結</span><span class="sxs-lookup"><span data-stu-id="49489-119">RELATED LINKS</span></span>

[<span data-ttu-id="49489-120">AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="49489-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="49489-121">移除-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="49489-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
