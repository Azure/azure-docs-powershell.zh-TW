---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454047"
---
# <span data-ttu-id="052e7-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="052e7-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="052e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="052e7-102">SYNOPSIS</span></span>
<span data-ttu-id="052e7-103">在網站復原中取得儲存分類。</span><span class="sxs-lookup"><span data-stu-id="052e7-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="052e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="052e7-104">SYNTAX</span></span>

### <span data-ttu-id="052e7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="052e7-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="052e7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="052e7-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="052e7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="052e7-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="052e7-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="052e7-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="052e7-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="052e7-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="052e7-110">說明</span><span class="sxs-lookup"><span data-stu-id="052e7-110">DESCRIPTION</span></span>
<span data-ttu-id="052e7-111">**AzureRmSiteRecoveryStorageClassification** Cmdlet 會取得 Azure Site Recovery 中的儲存分類。</span><span class="sxs-lookup"><span data-stu-id="052e7-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="052e7-112">示例</span><span class="sxs-lookup"><span data-stu-id="052e7-112">EXAMPLES</span></span>

## <span data-ttu-id="052e7-113">參數</span><span class="sxs-lookup"><span data-stu-id="052e7-113">PARAMETERS</span></span>

### <span data-ttu-id="052e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052e7-114">-DefaultProfile</span></span>
<span data-ttu-id="052e7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="052e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="052e7-116">-結構</span><span class="sxs-lookup"><span data-stu-id="052e7-116">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="052e7-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="052e7-117">-FriendlyName</span></span>
<span data-ttu-id="052e7-118">指定此 Cmdlet 所取得之儲存分類的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="052e7-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="052e7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="052e7-119">-Name</span></span>
<span data-ttu-id="052e7-120">指定此 Cmdlet 所取得之儲存分類的名稱。</span><span class="sxs-lookup"><span data-stu-id="052e7-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="052e7-121">-伺服器</span><span class="sxs-lookup"><span data-stu-id="052e7-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="052e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052e7-122">CommonParameters</span></span>
<span data-ttu-id="052e7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="052e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052e7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="052e7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052e7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="052e7-125">INPUTS</span></span>

### <span data-ttu-id="052e7-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="052e7-126">ASRFabric</span></span>
<span data-ttu-id="052e7-127">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="052e7-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="052e7-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="052e7-128">ASRServer</span></span>
<span data-ttu-id="052e7-129">形參 "Server" 接受管線中 "ASRServer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="052e7-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="052e7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="052e7-130">OUTPUTS</span></span>

### <span data-ttu-id="052e7-131">System.object. IEnumerable ' 1 [SiteRecovery. ASRStorageClassification] （）</span><span class="sxs-lookup"><span data-stu-id="052e7-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="052e7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="052e7-132">NOTES</span></span>

## <span data-ttu-id="052e7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="052e7-133">RELATED LINKS</span></span>

