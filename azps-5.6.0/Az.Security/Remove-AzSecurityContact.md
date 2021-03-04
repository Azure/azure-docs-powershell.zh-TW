---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: f8b96d8441e9a0b3a5f9b9bc3c775da7d71f12c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912314"
---
# <span data-ttu-id="6f1f2-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="6f1f2-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="6f1f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1f2-103">刪除安全性連絡人。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-103">Deletes a security contact.</span></span>

## <span data-ttu-id="6f1f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f1f2-104">SYNTAX</span></span>

### <span data-ttu-id="6f1f2-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="6f1f2-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f1f2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f1f2-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f1f2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6f1f2-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1f2-108">描述</span><span class="sxs-lookup"><span data-stu-id="6f1f2-108">DESCRIPTION</span></span>
<span data-ttu-id="6f1f2-109">刪除安全性連絡人。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-109">Deletes a security contact.</span></span>

## <span data-ttu-id="6f1f2-110">例子</span><span class="sxs-lookup"><span data-stu-id="6f1f2-110">EXAMPLES</span></span>

### <span data-ttu-id="6f1f2-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f1f2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="6f1f2-112">刪除「預設1」安全性連絡人</span><span class="sxs-lookup"><span data-stu-id="6f1f2-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="6f1f2-113">參數</span><span class="sxs-lookup"><span data-stu-id="6f1f2-113">PARAMETERS</span></span>

### <span data-ttu-id="6f1f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1f2-114">-DefaultProfile</span></span>
<span data-ttu-id="6f1f2-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f1f2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f1f2-116">-InputObject</span></span>
<span data-ttu-id="6f1f2-117">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1f2-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f1f2-118">-Name</span></span>
<span data-ttu-id="6f1f2-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-119">Resource name.</span></span>

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

### <span data-ttu-id="6f1f2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f1f2-120">-PassThru</span></span>
<span data-ttu-id="6f1f2-121">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-121">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1f2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f1f2-122">-ResourceId</span></span>
<span data-ttu-id="6f1f2-123">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-123">Resource ID.</span></span>

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

### <span data-ttu-id="6f1f2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="6f1f2-124">-Confirm</span></span>
<span data-ttu-id="6f1f2-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f1f2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1f2-126">-WhatIf</span></span>
<span data-ttu-id="6f1f2-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f1f2-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f1f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1f2-129">CommonParameters</span></span>
<span data-ttu-id="6f1f2-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f1f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1f2-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f1f2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1f2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6f1f2-132">INPUTS</span></span>

### <span data-ttu-id="6f1f2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6f1f2-133">System.String</span></span>

### <span data-ttu-id="6f1f2-134">Microsoft.Azure.Commands.Security.models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="6f1f2-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="6f1f2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="6f1f2-135">OUTPUTS</span></span>

### <span data-ttu-id="6f1f2-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f1f2-136">System.Boolean</span></span>

## <span data-ttu-id="6f1f2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="6f1f2-137">NOTES</span></span>

## <span data-ttu-id="6f1f2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f1f2-138">RELATED LINKS</span></span>
