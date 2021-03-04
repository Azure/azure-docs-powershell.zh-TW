---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b915be5c5014c278a2fbb12a6982890ed922ca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910634"
---
# <span data-ttu-id="b9828-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b9828-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b9828-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b9828-102">SYNOPSIS</span></span>
<span data-ttu-id="b9828-103">更新自動提供設定</span><span class="sxs-lookup"><span data-stu-id="b9828-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="b9828-104">語法</span><span class="sxs-lookup"><span data-stu-id="b9828-104">SYNTAX</span></span>

### <span data-ttu-id="b9828-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b9828-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9828-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9828-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9828-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9828-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9828-108">描述</span><span class="sxs-lookup"><span data-stu-id="b9828-108">DESCRIPTION</span></span>
<span data-ttu-id="b9828-109">開啟或關閉訂閱的自動撥備設定。</span><span class="sxs-lookup"><span data-stu-id="b9828-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="b9828-110">自動提供設定讓您決定是否要 Azure 資訊安全中心自動提供要安裝在您虛擬機器上的安全性代理程式。</span><span class="sxs-lookup"><span data-stu-id="b9828-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="b9828-111">安全性代理程式會監控您的 VM，以建立安全性警訊並監控 VM 的安全性合規性。</span><span class="sxs-lookup"><span data-stu-id="b9828-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="b9828-112">例子</span><span class="sxs-lookup"><span data-stu-id="b9828-112">EXAMPLES</span></span>

### <span data-ttu-id="b9828-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="b9828-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="b9828-114">開啟訂閱的自動設定。</span><span class="sxs-lookup"><span data-stu-id="b9828-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="b9828-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="b9828-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="b9828-116">關閉訂閱的自動資源設定。</span><span class="sxs-lookup"><span data-stu-id="b9828-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="b9828-117">參數</span><span class="sxs-lookup"><span data-stu-id="b9828-117">PARAMETERS</span></span>

### <span data-ttu-id="b9828-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9828-118">-DefaultProfile</span></span>
<span data-ttu-id="b9828-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9828-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9828-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="b9828-120">-EnableAutoProvision</span></span>
<span data-ttu-id="b9828-121">自動提供。</span><span class="sxs-lookup"><span data-stu-id="b9828-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9828-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9828-122">-InputObject</span></span>
<span data-ttu-id="b9828-123">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b9828-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9828-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9828-124">-Name</span></span>
<span data-ttu-id="b9828-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b9828-125">Resource name.</span></span>

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

### <span data-ttu-id="b9828-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9828-126">-ResourceId</span></span>
<span data-ttu-id="b9828-127">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9828-127">Resource ID.</span></span>

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

### <span data-ttu-id="b9828-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b9828-128">-Confirm</span></span>
<span data-ttu-id="b9828-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b9828-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9828-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9828-130">-WhatIf</span></span>
<span data-ttu-id="b9828-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9828-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9828-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9828-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9828-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9828-133">CommonParameters</span></span>
<span data-ttu-id="b9828-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b9828-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9828-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9828-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9828-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b9828-136">INPUTS</span></span>

### <span data-ttu-id="b9828-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b9828-137">System.String</span></span>

### <span data-ttu-id="b9828-138">Microsoft.Azure.Commands.Security.models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b9828-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b9828-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b9828-139">OUTPUTS</span></span>

### <span data-ttu-id="b9828-140">Microsoft.Azure.Commands.Security.models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b9828-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b9828-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b9828-141">NOTES</span></span>

## <span data-ttu-id="b9828-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9828-142">RELATED LINKS</span></span>
