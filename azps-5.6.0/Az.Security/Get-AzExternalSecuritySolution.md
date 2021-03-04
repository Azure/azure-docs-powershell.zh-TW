---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: a39fdd3c61c7060eec38d93f4d8ae07b6c9a1105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913329"
---
# <span data-ttu-id="d32e8-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d32e8-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="d32e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d32e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d32e8-103">取得外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d32e8-103">Get external security solution</span></span> 

## <span data-ttu-id="d32e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="d32e8-104">SYNTAX</span></span>

### <span data-ttu-id="d32e8-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="d32e8-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d32e8-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d32e8-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d32e8-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d32e8-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d32e8-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d32e8-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d32e8-109">描述</span><span class="sxs-lookup"><span data-stu-id="d32e8-109">DESCRIPTION</span></span>
<span data-ttu-id="d32e8-110">取得外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d32e8-110">Get external security solution</span></span>

## <span data-ttu-id="d32e8-111">例子</span><span class="sxs-lookup"><span data-stu-id="d32e8-111">EXAMPLES</span></span>

### <span data-ttu-id="d32e8-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d32e8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
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

<span data-ttu-id="d32e8-113">取得訂閱中所有的外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d32e8-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="d32e8-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d32e8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="d32e8-115">取得特定的外部安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="d32e8-115">Get a specific external security solution</span></span>

## <span data-ttu-id="d32e8-116">參數</span><span class="sxs-lookup"><span data-stu-id="d32e8-116">PARAMETERS</span></span>

### <span data-ttu-id="d32e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32e8-117">-DefaultProfile</span></span>
<span data-ttu-id="d32e8-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d32e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d32e8-119">-位置</span><span class="sxs-lookup"><span data-stu-id="d32e8-119">-Location</span></span>
<span data-ttu-id="d32e8-120">位置。</span><span class="sxs-lookup"><span data-stu-id="d32e8-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32e8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d32e8-121">-Name</span></span>
<span data-ttu-id="d32e8-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d32e8-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32e8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d32e8-123">-ResourceGroupName</span></span>
<span data-ttu-id="d32e8-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d32e8-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32e8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d32e8-125">-ResourceId</span></span>
<span data-ttu-id="d32e8-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d32e8-126">Resource ID.</span></span>

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

### <span data-ttu-id="d32e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32e8-127">CommonParameters</span></span>
<span data-ttu-id="d32e8-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d32e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32e8-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d32e8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32e8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d32e8-130">INPUTS</span></span>

### <span data-ttu-id="d32e8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d32e8-131">System.String</span></span>

## <span data-ttu-id="d32e8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d32e8-132">OUTPUTS</span></span>

### <span data-ttu-id="d32e8-133">Microsoft.Azure.Commands.Security.models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d32e8-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="d32e8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d32e8-134">NOTES</span></span>

## <span data-ttu-id="d32e8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d32e8-135">RELATED LINKS</span></span>
