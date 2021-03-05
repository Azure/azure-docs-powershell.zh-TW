---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1aeaba2f4f25abd49f12d087b7390f5e92f19c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917961"
---
# <span data-ttu-id="bf494-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bf494-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="bf494-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf494-102">SYNOPSIS</span></span>
<span data-ttu-id="bf494-103">取得 Azure 網站修復結構的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bf494-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="bf494-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf494-104">SYNTAX</span></span>

### <span data-ttu-id="bf494-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="bf494-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf494-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bf494-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf494-107">By有LylyName</span><span class="sxs-lookup"><span data-stu-id="bf494-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf494-108">描述</span><span class="sxs-lookup"><span data-stu-id="bf494-108">DESCRIPTION</span></span>
<span data-ttu-id="bf494-109">**Get-AzRecoveryServicesAsrFabric Cmdlet** 會取得指定 Azure 網站修復結構或復原服務庫中所有 Azure 網站修復布的屬性。</span><span class="sxs-lookup"><span data-stu-id="bf494-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="bf494-110">例子</span><span class="sxs-lookup"><span data-stu-id="bf494-110">EXAMPLES</span></span>

### <span data-ttu-id="bf494-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bf494-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="bf494-112">會回到儲存庫中的所有 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="bf494-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="bf494-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bf494-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="bf494-114">傳回名稱為 xxxx 的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="bf494-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="bf494-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="bf494-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="bf494-116">傳回 Azure 網站復原結構，並擁有好用的名稱 xxxx。</span><span class="sxs-lookup"><span data-stu-id="bf494-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="bf494-117">參數</span><span class="sxs-lookup"><span data-stu-id="bf494-117">PARAMETERS</span></span>

### <span data-ttu-id="bf494-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf494-118">-DefaultProfile</span></span>
<span data-ttu-id="bf494-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf494-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf494-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bf494-120">-FriendlyName</span></span>
<span data-ttu-id="bf494-121">以布料好用的名稱搜尋 ASR 布料。</span><span class="sxs-lookup"><span data-stu-id="bf494-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="bf494-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf494-122">-Name</span></span>
<span data-ttu-id="bf494-123">使用布料的名稱搜尋 ASR 布料。</span><span class="sxs-lookup"><span data-stu-id="bf494-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="bf494-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf494-124">CommonParameters</span></span>
<span data-ttu-id="bf494-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf494-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf494-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf494-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf494-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bf494-127">INPUTS</span></span>

### <span data-ttu-id="bf494-128">沒有</span><span class="sxs-lookup"><span data-stu-id="bf494-128">None</span></span>

## <span data-ttu-id="bf494-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bf494-129">OUTPUTS</span></span>

### <span data-ttu-id="bf494-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bf494-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bf494-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bf494-131">NOTES</span></span>

## <span data-ttu-id="bf494-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf494-132">RELATED LINKS</span></span>

[<span data-ttu-id="bf494-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bf494-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="bf494-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bf494-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
