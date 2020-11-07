---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625666"
---
# <span data-ttu-id="88572-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="88572-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="88572-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88572-102">SYNOPSIS</span></span>
<span data-ttu-id="88572-103">取得已登錄至目前電子倉庫之網站復原伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88572-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88572-104">句法</span><span class="sxs-lookup"><span data-stu-id="88572-104">SYNTAX</span></span>

### <span data-ttu-id="88572-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="88572-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88572-106">ByName</span><span class="sxs-lookup"><span data-stu-id="88572-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88572-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="88572-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88572-108">說明</span><span class="sxs-lookup"><span data-stu-id="88572-108">DESCRIPTION</span></span>
<span data-ttu-id="88572-109">**AzureRmSiteRecoveryServer** Cmdlet 會取得已登錄至目前網站復原電子倉庫之 Azure 網站復原伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88572-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="88572-110">示例</span><span class="sxs-lookup"><span data-stu-id="88572-110">EXAMPLES</span></span>

## <span data-ttu-id="88572-111">參數</span><span class="sxs-lookup"><span data-stu-id="88572-111">PARAMETERS</span></span>

### <span data-ttu-id="88572-112">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="88572-112">-FriendlyName</span></span>
<span data-ttu-id="88572-113">指定伺服器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="88572-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88572-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="88572-114">-Name</span></span>
<span data-ttu-id="88572-115">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="88572-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88572-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88572-116">-DefaultProfile</span></span>
<span data-ttu-id="88572-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88572-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88572-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88572-118">CommonParameters</span></span>
<span data-ttu-id="88572-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88572-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88572-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88572-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88572-121">輸入</span><span class="sxs-lookup"><span data-stu-id="88572-121">INPUTS</span></span>

## <span data-ttu-id="88572-122">輸出</span><span class="sxs-lookup"><span data-stu-id="88572-122">OUTPUTS</span></span>

### <span data-ttu-id="88572-123">System.object. IEnumerable ' 1 [SiteRecovery. ASRServer] （）</span><span class="sxs-lookup"><span data-stu-id="88572-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="88572-124">筆記</span><span class="sxs-lookup"><span data-stu-id="88572-124">NOTES</span></span>

## <span data-ttu-id="88572-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="88572-125">RELATED LINKS</span></span>

[<span data-ttu-id="88572-126">移除-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="88572-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
