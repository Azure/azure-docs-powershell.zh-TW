---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286424"
---
# <span data-ttu-id="be95e-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="be95e-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="be95e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be95e-102">SYNOPSIS</span></span>
<span data-ttu-id="be95e-103">取得 Azure 網站恢復結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="be95e-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="be95e-104">句法</span><span class="sxs-lookup"><span data-stu-id="be95e-104">SYNTAX</span></span>

### <span data-ttu-id="be95e-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="be95e-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be95e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="be95e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be95e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="be95e-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be95e-108">說明</span><span class="sxs-lookup"><span data-stu-id="be95e-108">DESCRIPTION</span></span>
<span data-ttu-id="be95e-109">**AzRecoveryServicesAsrFabric** Cmdlet 會取得指定 Azure 網站復原結構的屬性，或在恢復服務電子倉庫中的所有 azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="be95e-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="be95e-110">示例</span><span class="sxs-lookup"><span data-stu-id="be95e-110">EXAMPLES</span></span>

### <span data-ttu-id="be95e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="be95e-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="be95e-112">傳回保存庫中的所有 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="be95e-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="be95e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="be95e-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="be95e-114">使用名稱 xxxx 傳回 azure site recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="be95e-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="be95e-115">範例3</span><span class="sxs-lookup"><span data-stu-id="be95e-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="be95e-116">使用易記名稱 xxxx 傳回 azure site recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="be95e-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="be95e-117">參數</span><span class="sxs-lookup"><span data-stu-id="be95e-117">PARAMETERS</span></span>

### <span data-ttu-id="be95e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be95e-118">-DefaultProfile</span></span>
<span data-ttu-id="be95e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be95e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be95e-120">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="be95e-120">-FriendlyName</span></span>
<span data-ttu-id="be95e-121">依結構的易記名稱搜尋 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="be95e-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="be95e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="be95e-122">-Name</span></span>
<span data-ttu-id="be95e-123">透過結構的名稱搜尋 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="be95e-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="be95e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be95e-124">CommonParameters</span></span>
<span data-ttu-id="be95e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be95e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be95e-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be95e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be95e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="be95e-127">INPUTS</span></span>

### <span data-ttu-id="be95e-128">所有</span><span class="sxs-lookup"><span data-stu-id="be95e-128">None</span></span>

## <span data-ttu-id="be95e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="be95e-129">OUTPUTS</span></span>

### <span data-ttu-id="be95e-130">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="be95e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="be95e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="be95e-131">NOTES</span></span>

## <span data-ttu-id="be95e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="be95e-132">RELATED LINKS</span></span>

[<span data-ttu-id="be95e-133">新-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="be95e-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="be95e-134">移除-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="be95e-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
