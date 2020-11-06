---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454040"
---
# <span data-ttu-id="a1fc2-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a1fc2-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="a1fc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fc2-103">取得網站復原管理的虛擬機器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1fc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1fc2-104">SYNTAX</span></span>

### <span data-ttu-id="a1fc2-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="a1fc2-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1fc2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a1fc2-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1fc2-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1fc2-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1fc2-108">說明</span><span class="sxs-lookup"><span data-stu-id="a1fc2-108">DESCRIPTION</span></span>
<span data-ttu-id="a1fc2-109">**AzureRmSiteRecoveryVM** Cmdlet 會取得 Azure Site Recovery 中管理的虛擬機器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="a1fc2-110">示例</span><span class="sxs-lookup"><span data-stu-id="a1fc2-110">EXAMPLES</span></span>

## <span data-ttu-id="a1fc2-111">參數</span><span class="sxs-lookup"><span data-stu-id="a1fc2-111">PARAMETERS</span></span>

### <span data-ttu-id="a1fc2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fc2-112">-DefaultProfile</span></span>
<span data-ttu-id="a1fc2-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1fc2-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1fc2-114">-FriendlyName</span></span>
<span data-ttu-id="a1fc2-115">指定虛擬機器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-115">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fc2-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1fc2-116">-Name</span></span>
<span data-ttu-id="a1fc2-117">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fc2-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1fc2-118">-ProtectionContainer</span></span>
<span data-ttu-id="a1fc2-119">指定網站復原保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1fc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fc2-120">CommonParameters</span></span>
<span data-ttu-id="a1fc2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fc2-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1fc2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fc2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1fc2-123">INPUTS</span></span>

### <span data-ttu-id="a1fc2-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1fc2-124">ASRProtectionContainer</span></span>
<span data-ttu-id="a1fc2-125">形參 "ProtectionContainer" 接受管線中 "ASRProtectionContainer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a1fc2-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="a1fc2-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1fc2-126">ASRProtectionContainer</span></span>
<span data-ttu-id="a1fc2-127">形參 "ProtectionContainer" 接受管線中 "ASRProtectionContainer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a1fc2-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="a1fc2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a1fc2-128">OUTPUTS</span></span>

### <span data-ttu-id="a1fc2-129">System.object. IEnumerable ' 1 [SiteRecovery. ASRVirtualMachine] （）</span><span class="sxs-lookup"><span data-stu-id="a1fc2-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="a1fc2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a1fc2-130">NOTES</span></span>

## <span data-ttu-id="a1fc2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1fc2-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1fc2-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a1fc2-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
