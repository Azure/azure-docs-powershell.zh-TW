---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 588f9a057767e1e78b43664c35a61f26e6edf972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917922"
---
# <span data-ttu-id="caa8f-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="caa8f-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="caa8f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="caa8f-102">SYNOPSIS</span></span>

<span data-ttu-id="caa8f-103">在 Azure 資訊安全中心中為訂閱獲得 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="caa8f-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="caa8f-104">語法</span><span class="sxs-lookup"><span data-stu-id="caa8f-104">SYNTAX</span></span>

### <span data-ttu-id="caa8f-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="caa8f-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caa8f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="caa8f-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caa8f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="caa8f-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caa8f-108">描述</span><span class="sxs-lookup"><span data-stu-id="caa8f-108">DESCRIPTION</span></span>

<span data-ttu-id="caa8f-109">您可以使用此 Cmdlet 來查看每個訂閱的每個 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="caa8f-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="caa8f-110">有關 Azure Defender 和可用方案的詳細資訊，請參閱 [Azure Defender 簡介](https://docs.microsoft.com/azure/security-center/azure-defender)。</span><span class="sxs-lookup"><span data-stu-id="caa8f-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="caa8f-111">例子</span><span class="sxs-lookup"><span data-stu-id="caa8f-111">EXAMPLES</span></span>

### <span data-ttu-id="caa8f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="caa8f-112">Example 1</span></span>

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

<span data-ttu-id="caa8f-113">為訂閱獲得每個 Azure Defender 方案的狀態。</span><span class="sxs-lookup"><span data-stu-id="caa8f-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="caa8f-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="caa8f-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="caa8f-115">獲得特定資源識別碼的定價詳細資料。</span><span class="sxs-lookup"><span data-stu-id="caa8f-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="caa8f-116">其中 ResourceId 是其中一個由 . `Get-AzSecurityPricing`</span><span class="sxs-lookup"><span data-stu-id="caa8f-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="caa8f-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="caa8f-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="caa8f-118">獲得名稱為 Azure Defender 計畫的定價詳細資料。</span><span class="sxs-lookup"><span data-stu-id="caa8f-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="caa8f-119">其中 `name` 一個名稱會由 . `Get-AzSecurityPricing`</span><span class="sxs-lookup"><span data-stu-id="caa8f-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="caa8f-120">參數</span><span class="sxs-lookup"><span data-stu-id="caa8f-120">PARAMETERS</span></span>

### <span data-ttu-id="caa8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa8f-121">-DefaultProfile</span></span>

<span data-ttu-id="caa8f-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="caa8f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caa8f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="caa8f-123">-Name</span></span>

<span data-ttu-id="caa8f-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="caa8f-124">Resource name.</span></span>

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

### <span data-ttu-id="caa8f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caa8f-125">-ResourceId</span></span>

<span data-ttu-id="caa8f-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="caa8f-126">Resource ID.</span></span>

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

### <span data-ttu-id="caa8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa8f-127">CommonParameters</span></span>

<span data-ttu-id="caa8f-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="caa8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa8f-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="caa8f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa8f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="caa8f-130">INPUTS</span></span>

### <span data-ttu-id="caa8f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="caa8f-131">System.String</span></span>

## <span data-ttu-id="caa8f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="caa8f-132">OUTPUTS</span></span>

### <span data-ttu-id="caa8f-133">Microsoft.Azure.Commands.Security.models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="caa8f-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="caa8f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="caa8f-134">NOTES</span></span>

## <span data-ttu-id="caa8f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="caa8f-135">RELATED LINKS</span></span>
