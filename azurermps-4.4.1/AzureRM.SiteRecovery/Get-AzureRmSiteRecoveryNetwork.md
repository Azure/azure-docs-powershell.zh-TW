---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447958"
---
# <span data-ttu-id="d29e9-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d29e9-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="d29e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d29e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d29e9-103">取得目前電子倉庫的網站復原所管理網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d29e9-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d29e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d29e9-104">SYNTAX</span></span>

### <span data-ttu-id="d29e9-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="d29e9-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29e9-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="d29e9-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29e9-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="d29e9-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29e9-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="d29e9-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29e9-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="d29e9-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29e9-110">ByName</span><span class="sxs-lookup"><span data-stu-id="d29e9-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29e9-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d29e9-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d29e9-112">說明</span><span class="sxs-lookup"><span data-stu-id="d29e9-112">DESCRIPTION</span></span>
<span data-ttu-id="d29e9-113">**AzureRmSiteRecoveryNetwork** Cmdlet 會取得目前 Azure site recovery 保存庫的 Azure site recovery 網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d29e9-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d29e9-114">示例</span><span class="sxs-lookup"><span data-stu-id="d29e9-114">EXAMPLES</span></span>

## <span data-ttu-id="d29e9-115">參數</span><span class="sxs-lookup"><span data-stu-id="d29e9-115">PARAMETERS</span></span>

### <span data-ttu-id="d29e9-116">-結構</span><span class="sxs-lookup"><span data-stu-id="d29e9-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d29e9-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d29e9-117">-FriendlyName</span></span>
<span data-ttu-id="d29e9-118">指定虛擬機器網路的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="d29e9-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d29e9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d29e9-119">-Name</span></span>
<span data-ttu-id="d29e9-120">指定虛擬機器網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="d29e9-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d29e9-121">-伺服器</span><span class="sxs-lookup"><span data-stu-id="d29e9-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d29e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29e9-122">-DefaultProfile</span></span>
<span data-ttu-id="d29e9-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d29e9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29e9-124">CommonParameters</span></span>
<span data-ttu-id="d29e9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d29e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29e9-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d29e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29e9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d29e9-127">INPUTS</span></span>

### <span data-ttu-id="d29e9-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d29e9-128">ASRFabric</span></span>
<span data-ttu-id="d29e9-129">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d29e9-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="d29e9-130">字串</span><span class="sxs-lookup"><span data-stu-id="d29e9-130">String</span></span>
<span data-ttu-id="d29e9-131">參數「FriendlyName」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d29e9-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d29e9-132">字串</span><span class="sxs-lookup"><span data-stu-id="d29e9-132">String</span></span>
<span data-ttu-id="d29e9-133">參數「FriendlyName」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d29e9-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d29e9-134">字串</span><span class="sxs-lookup"><span data-stu-id="d29e9-134">String</span></span>
<span data-ttu-id="d29e9-135">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="d29e9-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d29e9-136">字串</span><span class="sxs-lookup"><span data-stu-id="d29e9-136">String</span></span>
<span data-ttu-id="d29e9-137">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="d29e9-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d29e9-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="d29e9-138">ASRServer</span></span>
<span data-ttu-id="d29e9-139">形參 "Server" 接受管線中 "ASRServer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d29e9-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="d29e9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d29e9-140">OUTPUTS</span></span>

### <span data-ttu-id="d29e9-141">System.object. IEnumerable ' 1 [SiteRecovery. ASRNetwork] （）</span><span class="sxs-lookup"><span data-stu-id="d29e9-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="d29e9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d29e9-142">NOTES</span></span>

## <span data-ttu-id="d29e9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d29e9-143">RELATED LINKS</span></span>

