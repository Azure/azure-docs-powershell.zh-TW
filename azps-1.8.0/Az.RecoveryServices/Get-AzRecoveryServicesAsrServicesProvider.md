---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621170"
---
# <span data-ttu-id="0c1dd-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0c1dd-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="0c1dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1dd-103">取得已登錄至 [恢復服務] 保存庫的 ASR 恢復服務提供者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="0c1dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c1dd-104">SYNTAX</span></span>

### <span data-ttu-id="0c1dd-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="0c1dd-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c1dd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0c1dd-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c1dd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0c1dd-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c1dd-108">說明</span><span class="sxs-lookup"><span data-stu-id="0c1dd-108">DESCRIPTION</span></span>
<span data-ttu-id="0c1dd-109">**AzRecoveryServicesAsrServicesProvider** Cmdlet 會取得保存庫中 Azure 網站恢復提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="0c1dd-110">示例</span><span class="sxs-lookup"><span data-stu-id="0c1dd-110">EXAMPLES</span></span>

### <span data-ttu-id="0c1dd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0c1dd-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="0c1dd-112">列出已登錄至 [恢復服務] 保存庫（對應至指定結構）的所有 ASR 複製服務提供者。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="0c1dd-113">參數</span><span class="sxs-lookup"><span data-stu-id="0c1dd-113">PARAMETERS</span></span>

### <span data-ttu-id="0c1dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1dd-114">-DefaultProfile</span></span>
<span data-ttu-id="0c1dd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1dd-116">-結構</span><span class="sxs-lookup"><span data-stu-id="0c1dd-116">-Fabric</span></span>
<span data-ttu-id="0c1dd-117">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1dd-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0c1dd-118">-FriendlyName</span></span>
<span data-ttu-id="0c1dd-119">指定 ASR 恢復服務提供者的易記名稱，以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="0c1dd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c1dd-120">-Name</span></span>
<span data-ttu-id="0c1dd-121">指定要取得詳細資料之 ASR 恢復服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="0c1dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1dd-122">CommonParameters</span></span>
<span data-ttu-id="0c1dd-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1dd-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c1dd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1dd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0c1dd-125">INPUTS</span></span>

### <span data-ttu-id="0c1dd-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0c1dd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0c1dd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0c1dd-127">OUTPUTS</span></span>

### <span data-ttu-id="0c1dd-128">RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0c1dd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="0c1dd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0c1dd-129">NOTES</span></span>

## <span data-ttu-id="0c1dd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c1dd-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c1dd-131">移除-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0c1dd-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="0c1dd-132">更新-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0c1dd-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
