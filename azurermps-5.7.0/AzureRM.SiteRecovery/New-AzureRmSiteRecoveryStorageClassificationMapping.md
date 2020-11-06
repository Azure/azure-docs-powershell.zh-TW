---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447634"
---
# <span data-ttu-id="43c33-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="43c33-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="43c33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43c33-102">SYNOPSIS</span></span>
<span data-ttu-id="43c33-103">在網站恢復中建立儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="43c33-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43c33-104">句法</span><span class="sxs-lookup"><span data-stu-id="43c33-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43c33-105">說明</span><span class="sxs-lookup"><span data-stu-id="43c33-105">DESCRIPTION</span></span>
<span data-ttu-id="43c33-106">**新的-AzureRmSiteRecoveryStorageClassificationMapping** Cmdlet 會在 Azure Site Recovery 中建立儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="43c33-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="43c33-107">示例</span><span class="sxs-lookup"><span data-stu-id="43c33-107">EXAMPLES</span></span>

## <span data-ttu-id="43c33-108">參數</span><span class="sxs-lookup"><span data-stu-id="43c33-108">PARAMETERS</span></span>

### <span data-ttu-id="43c33-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c33-109">-DefaultProfile</span></span>
<span data-ttu-id="43c33-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43c33-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c33-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="43c33-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c33-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="43c33-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="43c33-113">指定主要的儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="43c33-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c33-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="43c33-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="43c33-115">指定恢復儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="43c33-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c33-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c33-116">CommonParameters</span></span>
<span data-ttu-id="43c33-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43c33-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c33-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43c33-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c33-119">輸入</span><span class="sxs-lookup"><span data-stu-id="43c33-119">INPUTS</span></span>

### <span data-ttu-id="43c33-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="43c33-120">ASRStorageClassification</span></span>
<span data-ttu-id="43c33-121">形參 "PrimaryStorageClassification" 接受管線中 "ASRStorageClassification" 類型的值</span><span class="sxs-lookup"><span data-stu-id="43c33-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="43c33-122">輸出</span><span class="sxs-lookup"><span data-stu-id="43c33-122">OUTPUTS</span></span>

### <span data-ttu-id="43c33-123">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="43c33-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43c33-124">筆記</span><span class="sxs-lookup"><span data-stu-id="43c33-124">NOTES</span></span>

## <span data-ttu-id="43c33-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="43c33-125">RELATED LINKS</span></span>

[<span data-ttu-id="43c33-126">AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="43c33-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="43c33-127">移除-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="43c33-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
