---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b48222344e9a9fdb958073a658717d1cafa057f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916490"
---
# <span data-ttu-id="36e14-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="36e14-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="36e14-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36e14-102">SYNOPSIS</span></span>
<span data-ttu-id="36e14-103">獲得安全性自動撥備設定</span><span class="sxs-lookup"><span data-stu-id="36e14-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="36e14-104">語法</span><span class="sxs-lookup"><span data-stu-id="36e14-104">SYNTAX</span></span>

### <span data-ttu-id="36e14-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="36e14-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e14-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="36e14-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36e14-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e14-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36e14-108">描述</span><span class="sxs-lookup"><span data-stu-id="36e14-108">DESCRIPTION</span></span>
<span data-ttu-id="36e14-109">自動提供設定讓您決定是否要 Azure 資訊安全中心自動提供要安裝在您虛擬機器上的安全性代理程式。</span><span class="sxs-lookup"><span data-stu-id="36e14-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="36e14-110">安全性代理程式會監控您的 VM，以建立安全性警訊並監控 VM 的安全性合規性。</span><span class="sxs-lookup"><span data-stu-id="36e14-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="36e14-111">例子</span><span class="sxs-lookup"><span data-stu-id="36e14-111">EXAMPLES</span></span>

### <span data-ttu-id="36e14-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="36e14-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="36e14-113">獲得訂閱的自動設置設定</span><span class="sxs-lookup"><span data-stu-id="36e14-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="36e14-114">參數</span><span class="sxs-lookup"><span data-stu-id="36e14-114">PARAMETERS</span></span>

### <span data-ttu-id="36e14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e14-115">-DefaultProfile</span></span>
<span data-ttu-id="36e14-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36e14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e14-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="36e14-117">-Name</span></span>
<span data-ttu-id="36e14-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="36e14-118">Resource name.</span></span>

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

### <span data-ttu-id="36e14-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e14-119">-ResourceId</span></span>
<span data-ttu-id="36e14-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="36e14-120">Resource ID.</span></span>

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

### <span data-ttu-id="36e14-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e14-121">CommonParameters</span></span>
<span data-ttu-id="36e14-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36e14-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e14-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e14-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e14-124">輸入</span><span class="sxs-lookup"><span data-stu-id="36e14-124">INPUTS</span></span>

### <span data-ttu-id="36e14-125">System.String</span><span class="sxs-lookup"><span data-stu-id="36e14-125">System.String</span></span>

## <span data-ttu-id="36e14-126">輸出</span><span class="sxs-lookup"><span data-stu-id="36e14-126">OUTPUTS</span></span>

### <span data-ttu-id="36e14-127">Microsoft.Azure.Commands.Security.models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="36e14-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="36e14-128">筆記</span><span class="sxs-lookup"><span data-stu-id="36e14-128">NOTES</span></span>

## <span data-ttu-id="36e14-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="36e14-129">RELATED LINKS</span></span>
