---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137982"
---
# <span data-ttu-id="d8dc6-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d8dc6-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d8dc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dc6-103">取得安全性自動提供設定</span><span class="sxs-lookup"><span data-stu-id="d8dc6-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="d8dc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8dc6-104">SYNTAX</span></span>

### <span data-ttu-id="d8dc6-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="d8dc6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8dc6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d8dc6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dc6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dc6-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8dc6-108">說明</span><span class="sxs-lookup"><span data-stu-id="d8dc6-108">DESCRIPTION</span></span>
<span data-ttu-id="d8dc6-109">自動提供設定可讓您決定是否要讓 Azure 安全中心自動建立將在 Vm 上安裝的安全代理程式。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="d8dc6-110">安全性代理程式會監視您的 VM，以建立安全警示，並監視 VM 的安全性合規性。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="d8dc6-111">示例</span><span class="sxs-lookup"><span data-stu-id="d8dc6-111">EXAMPLES</span></span>

### <span data-ttu-id="d8dc6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d8dc6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="d8dc6-113">取得訂閱的自動預配設定</span><span class="sxs-lookup"><span data-stu-id="d8dc6-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="d8dc6-114">參數</span><span class="sxs-lookup"><span data-stu-id="d8dc6-114">PARAMETERS</span></span>

### <span data-ttu-id="d8dc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dc6-115">-DefaultProfile</span></span>
<span data-ttu-id="d8dc6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dc6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8dc6-117">-Name</span></span>
<span data-ttu-id="d8dc6-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-118">Resource name.</span></span>

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

### <span data-ttu-id="d8dc6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dc6-119">-ResourceId</span></span>
<span data-ttu-id="d8dc6-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-120">Resource ID.</span></span>

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

### <span data-ttu-id="d8dc6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dc6-121">CommonParameters</span></span>
<span data-ttu-id="d8dc6-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dc6-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dc6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d8dc6-124">INPUTS</span></span>

### <span data-ttu-id="d8dc6-125">System.object</span><span class="sxs-lookup"><span data-stu-id="d8dc6-125">System.String</span></span>

## <span data-ttu-id="d8dc6-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d8dc6-126">OUTPUTS</span></span>

### <span data-ttu-id="d8dc6-127">PSSecurityAutoProvisioningSetting 中的 AutoProvisioningSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="d8dc6-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d8dc6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d8dc6-128">NOTES</span></span>

## <span data-ttu-id="d8dc6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8dc6-129">RELATED LINKS</span></span>
