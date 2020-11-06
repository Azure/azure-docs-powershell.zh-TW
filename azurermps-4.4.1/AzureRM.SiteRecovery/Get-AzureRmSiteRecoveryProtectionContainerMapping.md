---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 869b22c881652680be31c541c6d70d95a45be43d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447955"
---
# <span data-ttu-id="502da-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="502da-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="502da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="502da-102">SYNOPSIS</span></span>
<span data-ttu-id="502da-103">取得 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="502da-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502da-104">句法</span><span class="sxs-lookup"><span data-stu-id="502da-104">SYNTAX</span></span>

### <span data-ttu-id="502da-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="502da-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="502da-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="502da-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="502da-107">說明</span><span class="sxs-lookup"><span data-stu-id="502da-107">DESCRIPTION</span></span>
<span data-ttu-id="502da-108">**AzureRmSiteRecoveryProtectionContainerMapping** Cmdlet 會將保護容器的相關資訊取得到保存庫中的策略映射。</span><span class="sxs-lookup"><span data-stu-id="502da-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="502da-109">示例</span><span class="sxs-lookup"><span data-stu-id="502da-109">EXAMPLES</span></span>

## <span data-ttu-id="502da-110">參數</span><span class="sxs-lookup"><span data-stu-id="502da-110">PARAMETERS</span></span>

### <span data-ttu-id="502da-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="502da-111">-Name</span></span>
<span data-ttu-id="502da-112">指定保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="502da-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502da-113">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="502da-113">-ProtectionContainer</span></span>
<span data-ttu-id="502da-114">指定 Azure Site Recovery 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="502da-114">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="502da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502da-115">-DefaultProfile</span></span>
<span data-ttu-id="502da-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="502da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="502da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502da-117">CommonParameters</span></span>
<span data-ttu-id="502da-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="502da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502da-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="502da-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502da-120">輸入</span><span class="sxs-lookup"><span data-stu-id="502da-120">INPUTS</span></span>

### <span data-ttu-id="502da-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="502da-121">ASRProtectionContainer</span></span>
<span data-ttu-id="502da-122">形參 "ProtectionContainer" 接受管線中 "ASRProtectionContainer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="502da-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="502da-123">輸出</span><span class="sxs-lookup"><span data-stu-id="502da-123">OUTPUTS</span></span>

### <span data-ttu-id="502da-124">System.object. IEnumerable "1 [ASRProtectionContainerMapping，SiteRecovery，Version = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （SiteRecovery =，Culture = 中立）</span><span class="sxs-lookup"><span data-stu-id="502da-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="502da-125">筆記</span><span class="sxs-lookup"><span data-stu-id="502da-125">NOTES</span></span>

## <span data-ttu-id="502da-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="502da-126">RELATED LINKS</span></span>

[<span data-ttu-id="502da-127">新-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="502da-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="502da-128">移除-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="502da-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
