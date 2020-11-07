---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623957"
---
# <span data-ttu-id="c6f9c-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c6f9c-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="c6f9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f9c-103">取得目前電子倉庫的網站復原所管理網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6f9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6f9c-104">SYNTAX</span></span>

### <span data-ttu-id="c6f9c-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c6f9c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f9c-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="c6f9c-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f9c-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="c6f9c-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f9c-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="c6f9c-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f9c-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="c6f9c-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f9c-110">ByName</span><span class="sxs-lookup"><span data-stu-id="c6f9c-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f9c-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c6f9c-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f9c-112">說明</span><span class="sxs-lookup"><span data-stu-id="c6f9c-112">DESCRIPTION</span></span>
<span data-ttu-id="c6f9c-113">**AzureRmSiteRecoveryNetwork** Cmdlet 會取得目前 Azure site recovery 保存庫的 Azure site recovery 網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c6f9c-114">示例</span><span class="sxs-lookup"><span data-stu-id="c6f9c-114">EXAMPLES</span></span>

## <span data-ttu-id="c6f9c-115">參數</span><span class="sxs-lookup"><span data-stu-id="c6f9c-115">PARAMETERS</span></span>

### <span data-ttu-id="c6f9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f9c-116">-DefaultProfile</span></span>
<span data-ttu-id="c6f9c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6f9c-118">-結構</span><span class="sxs-lookup"><span data-stu-id="c6f9c-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f9c-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c6f9c-119">-FriendlyName</span></span>
<span data-ttu-id="c6f9c-120">指定虛擬機器網路的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f9c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6f9c-121">-Name</span></span>
<span data-ttu-id="c6f9c-122">指定虛擬機器網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f9c-123">-伺服器</span><span class="sxs-lookup"><span data-stu-id="c6f9c-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f9c-124">CommonParameters</span></span>
<span data-ttu-id="c6f9c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f9c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6f9c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f9c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c6f9c-127">INPUTS</span></span>

### <span data-ttu-id="c6f9c-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c6f9c-128">ASRFabric</span></span>
<span data-ttu-id="c6f9c-129">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c6f9c-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="c6f9c-130">字串</span><span class="sxs-lookup"><span data-stu-id="c6f9c-130">String</span></span>
<span data-ttu-id="c6f9c-131">參數「FriendlyName」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c6f9c-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c6f9c-132">字串</span><span class="sxs-lookup"><span data-stu-id="c6f9c-132">String</span></span>
<span data-ttu-id="c6f9c-133">參數「FriendlyName」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c6f9c-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c6f9c-134">字串</span><span class="sxs-lookup"><span data-stu-id="c6f9c-134">String</span></span>
<span data-ttu-id="c6f9c-135">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="c6f9c-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c6f9c-136">字串</span><span class="sxs-lookup"><span data-stu-id="c6f9c-136">String</span></span>
<span data-ttu-id="c6f9c-137">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="c6f9c-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c6f9c-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="c6f9c-138">ASRServer</span></span>
<span data-ttu-id="c6f9c-139">形參 "Server" 接受管線中 "ASRServer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c6f9c-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="c6f9c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c6f9c-140">OUTPUTS</span></span>

### <span data-ttu-id="c6f9c-141">System.object. IEnumerable ' 1 [SiteRecovery. ASRNetwork] （）</span><span class="sxs-lookup"><span data-stu-id="c6f9c-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="c6f9c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c6f9c-142">NOTES</span></span>

## <span data-ttu-id="c6f9c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6f9c-143">RELATED LINKS</span></span>

