---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
ms.openlocfilehash: 4ef54651b5490161d7fc28c4a0c068f7b4a1ed76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451767"
---
# <span data-ttu-id="7d201-101">Get-AzureRmExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7d201-101">Get-AzureRmExternalSecuritySolution</span></span>

## <span data-ttu-id="7d201-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d201-102">SYNOPSIS</span></span>
<span data-ttu-id="7d201-103">取得外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="7d201-103">Get external security solution</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d201-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d201-104">SYNTAX</span></span>

### <span data-ttu-id="7d201-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="7d201-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d201-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="7d201-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d201-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7d201-107">SubscriptionLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d201-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d201-108">ResourceId</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d201-109">說明</span><span class="sxs-lookup"><span data-stu-id="7d201-109">DESCRIPTION</span></span>
<span data-ttu-id="7d201-110">取得外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="7d201-110">Get external security solution</span></span>

## <span data-ttu-id="7d201-111">示例</span><span class="sxs-lookup"><span data-stu-id="7d201-111">EXAMPLES</span></span>

### <span data-ttu-id="7d201-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7d201-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="7d201-113">取得訂閱中的所有外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="7d201-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="7d201-114">範例2</span><span class="sxs-lookup"><span data-stu-id="7d201-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="7d201-115">取得特定的外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="7d201-115">Get a specific external security solution</span></span>

## <span data-ttu-id="7d201-116">參數</span><span class="sxs-lookup"><span data-stu-id="7d201-116">PARAMETERS</span></span>

### <span data-ttu-id="7d201-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d201-117">-DefaultProfile</span></span>
<span data-ttu-id="7d201-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d201-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d201-119">-位置</span><span class="sxs-lookup"><span data-stu-id="7d201-119">-Location</span></span>
<span data-ttu-id="7d201-120">位於.</span><span class="sxs-lookup"><span data-stu-id="7d201-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d201-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d201-121">-Name</span></span>
<span data-ttu-id="7d201-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7d201-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d201-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d201-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d201-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7d201-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d201-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d201-125">-ResourceId</span></span>
<span data-ttu-id="7d201-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7d201-126">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d201-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d201-127">CommonParameters</span></span>
<span data-ttu-id="7d201-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d201-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d201-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d201-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d201-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7d201-130">INPUTS</span></span>

### <span data-ttu-id="7d201-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7d201-131">System.String</span></span>

## <span data-ttu-id="7d201-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7d201-132">OUTPUTS</span></span>

### <span data-ttu-id="7d201-133">PSSecurityExternalSecuritySolution 中的 ExternalSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="7d201-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="7d201-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7d201-134">NOTES</span></span>

## <span data-ttu-id="7d201-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d201-135">RELATED LINKS</span></span>
