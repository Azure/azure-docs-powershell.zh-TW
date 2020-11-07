---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3eb55379b84570ad49bbea038b4264345508c82c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623964"
---
# <span data-ttu-id="adfc3-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="adfc3-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="adfc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="adfc3-103">取得已登錄至 [恢復服務] 保存庫的 ASR 恢復服務提供者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="adfc3-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adfc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="adfc3-104">SYNTAX</span></span>

### <span data-ttu-id="adfc3-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="adfc3-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="adfc3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="adfc3-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adfc3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="adfc3-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adfc3-108">說明</span><span class="sxs-lookup"><span data-stu-id="adfc3-108">DESCRIPTION</span></span>
<span data-ttu-id="adfc3-109">**AzureRmRecoveryServicesAsrServicesProvider** Cmdlet 會取得保存庫中 Azure 網站恢復提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="adfc3-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="adfc3-110">示例</span><span class="sxs-lookup"><span data-stu-id="adfc3-110">EXAMPLES</span></span>

### <span data-ttu-id="adfc3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="adfc3-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="adfc3-112">列出已登錄至 [恢復服務] 保存庫（對應至指定結構）的所有 ASR 複製服務提供者。</span><span class="sxs-lookup"><span data-stu-id="adfc3-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="adfc3-113">參數</span><span class="sxs-lookup"><span data-stu-id="adfc3-113">PARAMETERS</span></span>

### <span data-ttu-id="adfc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfc3-114">-DefaultProfile</span></span>
<span data-ttu-id="adfc3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="adfc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="adfc3-116">-結構</span><span class="sxs-lookup"><span data-stu-id="adfc3-116">-Fabric</span></span>
<span data-ttu-id="adfc3-117">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="adfc3-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adfc3-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="adfc3-118">-FriendlyName</span></span>
<span data-ttu-id="adfc3-119">指定 ASR 恢復服務提供者的易記名稱，以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="adfc3-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="adfc3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="adfc3-120">-Name</span></span>
<span data-ttu-id="adfc3-121">指定要取得詳細資料之 ASR 恢復服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="adfc3-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="adfc3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfc3-122">CommonParameters</span></span>
<span data-ttu-id="adfc3-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adfc3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfc3-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="adfc3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfc3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="adfc3-125">INPUTS</span></span>

### <span data-ttu-id="adfc3-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="adfc3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="adfc3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="adfc3-127">OUTPUTS</span></span>

### <span data-ttu-id="adfc3-128">System.object. IEnumerable "1 [ASRRecoveryServicesProvider，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="adfc3-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="adfc3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="adfc3-129">NOTES</span></span>

## <span data-ttu-id="adfc3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="adfc3-130">RELATED LINKS</span></span>

[<span data-ttu-id="adfc3-131">移除-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="adfc3-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="adfc3-132">更新-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="adfc3-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
