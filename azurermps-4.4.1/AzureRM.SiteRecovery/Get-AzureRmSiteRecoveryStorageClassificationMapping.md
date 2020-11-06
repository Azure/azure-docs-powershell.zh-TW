---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454827"
---
# <span data-ttu-id="c9b55-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c9b55-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="c9b55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9b55-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b55-103">在網站復原中取得儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="c9b55-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b55-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9b55-104">SYNTAX</span></span>

### <span data-ttu-id="c9b55-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c9b55-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9b55-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c9b55-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9b55-107">說明</span><span class="sxs-lookup"><span data-stu-id="c9b55-107">DESCRIPTION</span></span>
<span data-ttu-id="c9b55-108">**AzureRmSiteRecoveryStorageClassificationMapping** Cmdlet 會取得 Azure Site Recovery 中的儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="c9b55-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="c9b55-109">示例</span><span class="sxs-lookup"><span data-stu-id="c9b55-109">EXAMPLES</span></span>

## <span data-ttu-id="c9b55-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9b55-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b55-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9b55-111">-Name</span></span>
<span data-ttu-id="c9b55-112">指定此 Cmdlet 所取得之儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9b55-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c9b55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b55-113">-DefaultProfile</span></span>
<span data-ttu-id="c9b55-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9b55-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9b55-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b55-115">CommonParameters</span></span>
<span data-ttu-id="c9b55-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9b55-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b55-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9b55-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b55-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c9b55-118">INPUTS</span></span>

## <span data-ttu-id="c9b55-119">輸出</span><span class="sxs-lookup"><span data-stu-id="c9b55-119">OUTPUTS</span></span>

### <span data-ttu-id="c9b55-120">System.object. IEnumerable ' 1 [SiteRecovery. ASRStorageClassificationMapping] （）</span><span class="sxs-lookup"><span data-stu-id="c9b55-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="c9b55-121">筆記</span><span class="sxs-lookup"><span data-stu-id="c9b55-121">NOTES</span></span>

## <span data-ttu-id="c9b55-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9b55-122">RELATED LINKS</span></span>

[<span data-ttu-id="c9b55-123">新-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c9b55-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="c9b55-124">移除-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c9b55-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
