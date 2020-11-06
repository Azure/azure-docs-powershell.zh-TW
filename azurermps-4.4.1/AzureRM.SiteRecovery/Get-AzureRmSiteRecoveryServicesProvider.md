---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e61136122873f7837120065194252aba145ea733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454828"
---
# <span data-ttu-id="f75be-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f75be-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="f75be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f75be-102">SYNOPSIS</span></span>
<span data-ttu-id="f75be-103">取得有關保存庫中 Azure 網站恢復提供者的資訊。</span><span class="sxs-lookup"><span data-stu-id="f75be-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f75be-104">句法</span><span class="sxs-lookup"><span data-stu-id="f75be-104">SYNTAX</span></span>

### <span data-ttu-id="f75be-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f75be-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f75be-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f75be-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f75be-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f75be-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f75be-108">說明</span><span class="sxs-lookup"><span data-stu-id="f75be-108">DESCRIPTION</span></span>
<span data-ttu-id="f75be-109">**AzureRmSiteRecoveryServicesProvider** Cmdlet 會取得保存庫中 Azure 網站恢復提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f75be-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="f75be-110">示例</span><span class="sxs-lookup"><span data-stu-id="f75be-110">EXAMPLES</span></span>

## <span data-ttu-id="f75be-111">參數</span><span class="sxs-lookup"><span data-stu-id="f75be-111">PARAMETERS</span></span>

### <span data-ttu-id="f75be-112">-結構</span><span class="sxs-lookup"><span data-stu-id="f75be-112">-Fabric</span></span>
<span data-ttu-id="f75be-113">指定 Azure Site Recovery Fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="f75be-113">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f75be-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f75be-114">-FriendlyName</span></span>
<span data-ttu-id="f75be-115">指定此 Cmdlet 取得之 Azure Site Recovery 提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f75be-115">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f75be-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f75be-116">-Name</span></span>
<span data-ttu-id="f75be-117">指定此 Cmdlet 所取得之 Azure Site Recovery 提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75be-117">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f75be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75be-118">-DefaultProfile</span></span>
<span data-ttu-id="f75be-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f75be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f75be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75be-120">CommonParameters</span></span>
<span data-ttu-id="f75be-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f75be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75be-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f75be-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75be-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f75be-123">INPUTS</span></span>

### <span data-ttu-id="f75be-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f75be-124">ASRFabric</span></span>
<span data-ttu-id="f75be-125">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f75be-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="f75be-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f75be-126">OUTPUTS</span></span>

### <span data-ttu-id="f75be-127">System.object. IEnumerable "1 [ASRRecoveryServicesProvider，SiteRecovery，Version = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （SiteRecovery =，Culture = 中立）</span><span class="sxs-lookup"><span data-stu-id="f75be-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f75be-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f75be-128">NOTES</span></span>

## <span data-ttu-id="f75be-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f75be-129">RELATED LINKS</span></span>

[<span data-ttu-id="f75be-130">移除-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f75be-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="f75be-131">更新-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f75be-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
