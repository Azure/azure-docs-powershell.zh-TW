---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970192"
---
# <span data-ttu-id="4a82e-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="4a82e-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="4a82e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a82e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a82e-103">取得安全性自動提供設定</span><span class="sxs-lookup"><span data-stu-id="4a82e-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="4a82e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a82e-104">SYNTAX</span></span>

### <span data-ttu-id="4a82e-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="4a82e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a82e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4a82e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a82e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a82e-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a82e-108">說明</span><span class="sxs-lookup"><span data-stu-id="4a82e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a82e-109">自動提供設定可讓您決定是否要讓 Azure 安全中心自動建立將在 Vm 上安裝的安全代理程式。</span><span class="sxs-lookup"><span data-stu-id="4a82e-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="4a82e-110">安全性代理程式會監視您的 VM，以建立安全警示，並監視 VM 的安全性合規性。</span><span class="sxs-lookup"><span data-stu-id="4a82e-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="4a82e-111">示例</span><span class="sxs-lookup"><span data-stu-id="4a82e-111">EXAMPLES</span></span>

### <span data-ttu-id="4a82e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="4a82e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="4a82e-113">取得訂閱的自動預配設定</span><span class="sxs-lookup"><span data-stu-id="4a82e-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="4a82e-114">參數</span><span class="sxs-lookup"><span data-stu-id="4a82e-114">PARAMETERS</span></span>

### <span data-ttu-id="4a82e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a82e-115">-DefaultProfile</span></span>
<span data-ttu-id="4a82e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a82e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a82e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a82e-117">-Name</span></span>
<span data-ttu-id="4a82e-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4a82e-118">Resource name.</span></span>

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

### <span data-ttu-id="4a82e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a82e-119">-ResourceId</span></span>
<span data-ttu-id="4a82e-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4a82e-120">Resource ID.</span></span>

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

### <span data-ttu-id="4a82e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a82e-121">CommonParameters</span></span>
<span data-ttu-id="4a82e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a82e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a82e-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4a82e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a82e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4a82e-124">INPUTS</span></span>

### <span data-ttu-id="4a82e-125">System.object</span><span class="sxs-lookup"><span data-stu-id="4a82e-125">System.String</span></span>

## <span data-ttu-id="4a82e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4a82e-126">OUTPUTS</span></span>

### <span data-ttu-id="4a82e-127">PSSecurityAutoProvisioningSetting 中的 AutoProvisioningSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="4a82e-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="4a82e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4a82e-128">NOTES</span></span>

## <span data-ttu-id="4a82e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a82e-129">RELATED LINKS</span></span>
