---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456376"
---
# <span data-ttu-id="4d100-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4d100-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="4d100-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d100-102">SYNOPSIS</span></span>
<span data-ttu-id="4d100-103">取得目前網站復原電子倉庫中受保護或受保護實體的清單。</span><span class="sxs-lookup"><span data-stu-id="4d100-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d100-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d100-104">SYNTAX</span></span>

### <span data-ttu-id="4d100-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="4d100-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d100-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4d100-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d100-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4d100-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d100-108">說明</span><span class="sxs-lookup"><span data-stu-id="4d100-108">DESCRIPTION</span></span>
<span data-ttu-id="4d100-109">**AzureRmSiteRecoveryProtectionEntity** Cmdlet 會在目前的 Azure Site Recovery 保存庫中取得可存取或受保護實體的清單（例如虛擬機器）。</span><span class="sxs-lookup"><span data-stu-id="4d100-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4d100-110">示例</span><span class="sxs-lookup"><span data-stu-id="4d100-110">EXAMPLES</span></span>

## <span data-ttu-id="4d100-111">參數</span><span class="sxs-lookup"><span data-stu-id="4d100-111">PARAMETERS</span></span>

### <span data-ttu-id="4d100-112">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4d100-112">-FriendlyName</span></span>
<span data-ttu-id="4d100-113">指定保護實體的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4d100-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d100-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d100-114">-Name</span></span>
<span data-ttu-id="4d100-115">指定保護實體的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d100-115">Specifies the name of the protection entity.</span></span>

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

### <span data-ttu-id="4d100-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4d100-116">-ProtectionContainer</span></span>
<span data-ttu-id="4d100-117">指定保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="4d100-117">Specifies the protection container object.</span></span>

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

### <span data-ttu-id="4d100-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d100-118">-DefaultProfile</span></span>
<span data-ttu-id="4d100-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d100-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d100-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d100-120">CommonParameters</span></span>
<span data-ttu-id="4d100-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d100-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d100-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d100-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d100-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4d100-123">INPUTS</span></span>

### <span data-ttu-id="4d100-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4d100-124">ASRProtectionContainer</span></span>
<span data-ttu-id="4d100-125">形參 "ProtectionContainer" 接受管線中 "ASRProtectionContainer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4d100-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="4d100-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4d100-126">OUTPUTS</span></span>

### <span data-ttu-id="4d100-127">System.object. IEnumerable ' 1 [SiteRecovery. ASRProtectionEntity] （）</span><span class="sxs-lookup"><span data-stu-id="4d100-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="4d100-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4d100-128">NOTES</span></span>

## <span data-ttu-id="4d100-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d100-129">RELATED LINKS</span></span>

[<span data-ttu-id="4d100-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4d100-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
