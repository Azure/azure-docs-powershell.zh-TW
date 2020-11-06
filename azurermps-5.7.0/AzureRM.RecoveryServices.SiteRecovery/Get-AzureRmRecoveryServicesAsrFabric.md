---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 92631a1a6c5d27953777efe2b6ea158f59da8fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446079"
---
# <span data-ttu-id="9b3f8-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9b3f8-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="9b3f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3f8-103">取得 Azure 網站恢復結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b3f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b3f8-104">SYNTAX</span></span>

### <span data-ttu-id="9b3f8-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="9b3f8-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b3f8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9b3f8-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b3f8-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9b3f8-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b3f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b3f8-108">DESCRIPTION</span></span>
<span data-ttu-id="9b3f8-109">**AzureRmRecoveryServicesAsrFabric** Cmdlet 會取得指定 Azure 網站復原結構的屬性，或在恢復服務電子倉庫中的所有 azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="9b3f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b3f8-110">EXAMPLES</span></span>

### <span data-ttu-id="9b3f8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9b3f8-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="9b3f8-112">傳回保存庫中的所有 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="9b3f8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9b3f8-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="9b3f8-114">使用名稱 xxxx 傳回 azure site recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="9b3f8-115">範例3</span><span class="sxs-lookup"><span data-stu-id="9b3f8-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="9b3f8-116">使用易記名稱 xxxx 傳回 azure site recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="9b3f8-117">參數</span><span class="sxs-lookup"><span data-stu-id="9b3f8-117">PARAMETERS</span></span>

### <span data-ttu-id="9b3f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3f8-118">-DefaultProfile</span></span>
<span data-ttu-id="9b3f8-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="9b3f8-120">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9b3f8-120">-FriendlyName</span></span>
<span data-ttu-id="9b3f8-121">依結構的易記名稱搜尋 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="9b3f8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b3f8-122">-Name</span></span>
<span data-ttu-id="9b3f8-123">透過結構的名稱搜尋 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="9b3f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3f8-124">CommonParameters</span></span>
<span data-ttu-id="9b3f8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3f8-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b3f8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3f8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b3f8-127">INPUTS</span></span>

### <span data-ttu-id="9b3f8-128">所有</span><span class="sxs-lookup"><span data-stu-id="9b3f8-128">None</span></span>

## <span data-ttu-id="9b3f8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9b3f8-129">OUTPUTS</span></span>

### <span data-ttu-id="9b3f8-130">[System.object]. 清單 ' 1 [RecoveryServices. SiteRecovery，ASRFabric，，RecoveryServices. SiteRecovery，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9b3f8-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9b3f8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9b3f8-131">NOTES</span></span>

## <span data-ttu-id="9b3f8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b3f8-132">RELATED LINKS</span></span>

[<span data-ttu-id="9b3f8-133">新-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9b3f8-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="9b3f8-134">移除-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9b3f8-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
