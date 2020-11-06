---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450469"
---
# <span data-ttu-id="d74e4-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d74e4-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="d74e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d74e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d74e4-103">從網站復原中移除儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="d74e4-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d74e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d74e4-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d74e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="d74e4-105">DESCRIPTION</span></span>
<span data-ttu-id="d74e4-106">**AzureRmSiteRecoveryStorageClassificationMapping** Cmdlet 會從 Azure Site Recovery 中移除儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="d74e4-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="d74e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="d74e4-107">EXAMPLES</span></span>

## <span data-ttu-id="d74e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="d74e4-108">PARAMETERS</span></span>

### <span data-ttu-id="d74e4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74e4-109">-DefaultProfile</span></span>
<span data-ttu-id="d74e4-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d74e4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d74e4-111">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d74e4-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="d74e4-112">指定此 Cmdlet 移除的儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="d74e4-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d74e4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74e4-113">CommonParameters</span></span>
<span data-ttu-id="d74e4-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d74e4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74e4-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d74e4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74e4-116">輸入</span><span class="sxs-lookup"><span data-stu-id="d74e4-116">INPUTS</span></span>

### <span data-ttu-id="d74e4-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d74e4-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="d74e4-118">形參 "StorageClassificationMapping" 接受管線中 "ASRStorageClassificationMapping" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d74e4-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="d74e4-119">輸出</span><span class="sxs-lookup"><span data-stu-id="d74e4-119">OUTPUTS</span></span>

### <span data-ttu-id="d74e4-120">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d74e4-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d74e4-121">筆記</span><span class="sxs-lookup"><span data-stu-id="d74e4-121">NOTES</span></span>

## <span data-ttu-id="d74e4-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="d74e4-122">RELATED LINKS</span></span>

[<span data-ttu-id="d74e4-123">AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d74e4-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="d74e4-124">新-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d74e4-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)