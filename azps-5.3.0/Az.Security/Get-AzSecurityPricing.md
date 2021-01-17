---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448683"
---
# <span data-ttu-id="8e9c8-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="8e9c8-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="8e9c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e9c8-102">SYNOPSIS</span></span>

<span data-ttu-id="8e9c8-103">取得 Azure 安全中心訂閱的 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="8e9c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e9c8-104">SYNTAX</span></span>

### <span data-ttu-id="8e9c8-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="8e9c8-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9c8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8e9c8-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9c8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9c8-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e9c8-108">說明</span><span class="sxs-lookup"><span data-stu-id="8e9c8-108">DESCRIPTION</span></span>

<span data-ttu-id="8e9c8-109">您可以使用此 Cmdlet 來查看每個 Azure Defender 方案（依訂閱）。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="8e9c8-110">如需 Azure Defender 和可用方案的詳細資訊，請參閱 [Azure Defender 簡介](https://docs.microsoft.com/azure/security-center/azure-defender)。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="8e9c8-111">示例</span><span class="sxs-lookup"><span data-stu-id="8e9c8-111">EXAMPLES</span></span>

### <span data-ttu-id="8e9c8-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8e9c8-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="8e9c8-113">取得訂閱的每個 Azure Defender 方案的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="8e9c8-114">範例2</span><span class="sxs-lookup"><span data-stu-id="8e9c8-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="8e9c8-115">取得特定資源識別碼的定價詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="8e9c8-116">[ResourceId] 是傳回的其中一個識別碼 `Get-AzSecurityPricing` 。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="8e9c8-117">範例3</span><span class="sxs-lookup"><span data-stu-id="8e9c8-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="8e9c8-118">取得命名 Azure Defender 方案的定價詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="8e9c8-119">其中 `name` 會傳回其中一個名稱的位置 `Get-AzSecurityPricing` 。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="8e9c8-120">參數</span><span class="sxs-lookup"><span data-stu-id="8e9c8-120">PARAMETERS</span></span>

### <span data-ttu-id="8e9c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9c8-121">-DefaultProfile</span></span>

<span data-ttu-id="8e9c8-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9c8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e9c8-123">-Name</span></span>

<span data-ttu-id="8e9c8-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9c8-125">-ResourceId</span></span>

<span data-ttu-id="8e9c8-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9c8-127">CommonParameters</span></span>

<span data-ttu-id="8e9c8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9c8-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9c8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8e9c8-130">INPUTS</span></span>

### <span data-ttu-id="8e9c8-131">System.object</span><span class="sxs-lookup"><span data-stu-id="8e9c8-131">System.String</span></span>

## <span data-ttu-id="8e9c8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8e9c8-132">OUTPUTS</span></span>

### <span data-ttu-id="8e9c8-133">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="8e9c8-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="8e9c8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8e9c8-134">NOTES</span></span>

## <span data-ttu-id="8e9c8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e9c8-135">RELATED LINKS</span></span>
