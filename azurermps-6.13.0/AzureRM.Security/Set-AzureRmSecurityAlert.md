---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448222"
---
# <span data-ttu-id="341f3-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="341f3-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="341f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="341f3-102">SYNOPSIS</span></span>
<span data-ttu-id="341f3-103">更新安全警示狀態。</span><span class="sxs-lookup"><span data-stu-id="341f3-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="341f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="341f3-104">SYNTAX</span></span>

### <span data-ttu-id="341f3-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="341f3-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341f3-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="341f3-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341f3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="341f3-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341f3-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="341f3-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="341f3-109">說明</span><span class="sxs-lookup"><span data-stu-id="341f3-109">DESCRIPTION</span></span>
<span data-ttu-id="341f3-110">設定安全性警示狀態。</span><span class="sxs-lookup"><span data-stu-id="341f3-110">Sets a security alert state.</span></span>

## <span data-ttu-id="341f3-111">示例</span><span class="sxs-lookup"><span data-stu-id="341f3-111">EXAMPLES</span></span>

### <span data-ttu-id="341f3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="341f3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="341f3-113">關閉引發的安全性警示。</span><span class="sxs-lookup"><span data-stu-id="341f3-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="341f3-114">參數</span><span class="sxs-lookup"><span data-stu-id="341f3-114">PARAMETERS</span></span>

### <span data-ttu-id="341f3-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="341f3-115">-ActionType</span></span>
<span data-ttu-id="341f3-116">動作類型。</span><span class="sxs-lookup"><span data-stu-id="341f3-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341f3-117">-DefaultProfile</span></span>
<span data-ttu-id="341f3-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="341f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="341f3-119">-InputObject</span></span>
<span data-ttu-id="341f3-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="341f3-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-121">-位置</span><span class="sxs-lookup"><span data-stu-id="341f3-121">-Location</span></span>
<span data-ttu-id="341f3-122">位於.</span><span class="sxs-lookup"><span data-stu-id="341f3-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="341f3-123">-Name</span></span>
<span data-ttu-id="341f3-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="341f3-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="341f3-125">-PassThru</span></span>
<span data-ttu-id="341f3-126">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="341f3-126">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="341f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="341f3-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="341f3-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="341f3-129">-ResourceId</span></span>
<span data-ttu-id="341f3-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="341f3-130">Resource ID.</span></span>

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

### <span data-ttu-id="341f3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="341f3-131">-Confirm</span></span>
<span data-ttu-id="341f3-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="341f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="341f3-133">-WhatIf</span></span>
<span data-ttu-id="341f3-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="341f3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="341f3-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="341f3-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341f3-136">CommonParameters</span></span>
<span data-ttu-id="341f3-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="341f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341f3-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="341f3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341f3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="341f3-139">INPUTS</span></span>

### <span data-ttu-id="341f3-140">System.object</span><span class="sxs-lookup"><span data-stu-id="341f3-140">System.String</span></span>
<span data-ttu-id="341f3-141">PSSetAlertInputObject （Security）命令。</span><span class="sxs-lookup"><span data-stu-id="341f3-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="341f3-142">輸出</span><span class="sxs-lookup"><span data-stu-id="341f3-142">OUTPUTS</span></span>

### <span data-ttu-id="341f3-143">PSSecurityAlert （Security. 命令）。</span><span class="sxs-lookup"><span data-stu-id="341f3-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="341f3-144">筆記</span><span class="sxs-lookup"><span data-stu-id="341f3-144">NOTES</span></span>

## <span data-ttu-id="341f3-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="341f3-145">RELATED LINKS</span></span>
