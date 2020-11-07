---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: eac99fc2395408f2e140b3369a87e75928006f21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791081"
---
# <span data-ttu-id="5948d-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="5948d-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="5948d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5948d-102">SYNOPSIS</span></span>
<span data-ttu-id="5948d-103">刪除安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="5948d-103">Deletes a security contact.</span></span>

## <span data-ttu-id="5948d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5948d-104">SYNTAX</span></span>

### <span data-ttu-id="5948d-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5948d-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5948d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5948d-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5948d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5948d-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5948d-108">說明</span><span class="sxs-lookup"><span data-stu-id="5948d-108">DESCRIPTION</span></span>
<span data-ttu-id="5948d-109">刪除安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="5948d-109">Deletes a security contact.</span></span>

## <span data-ttu-id="5948d-110">示例</span><span class="sxs-lookup"><span data-stu-id="5948d-110">EXAMPLES</span></span>

### <span data-ttu-id="5948d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5948d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="5948d-112">刪除「default1」安全連絡人</span><span class="sxs-lookup"><span data-stu-id="5948d-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="5948d-113">參數</span><span class="sxs-lookup"><span data-stu-id="5948d-113">PARAMETERS</span></span>

### <span data-ttu-id="5948d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5948d-114">-DefaultProfile</span></span>
<span data-ttu-id="5948d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5948d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5948d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5948d-116">-InputObject</span></span>
<span data-ttu-id="5948d-117">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="5948d-117">Input Object.</span></span>

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

### <span data-ttu-id="5948d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5948d-118">-Name</span></span>
<span data-ttu-id="5948d-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5948d-119">Resource name.</span></span>

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

### <span data-ttu-id="5948d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5948d-120">-PassThru</span></span>
<span data-ttu-id="5948d-121">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="5948d-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5948d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5948d-122">-ResourceId</span></span>
<span data-ttu-id="5948d-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5948d-123">Resource ID.</span></span>

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

### <span data-ttu-id="5948d-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5948d-124">-Confirm</span></span>
<span data-ttu-id="5948d-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5948d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5948d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5948d-126">-WhatIf</span></span>
<span data-ttu-id="5948d-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5948d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5948d-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5948d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5948d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5948d-129">CommonParameters</span></span>
<span data-ttu-id="5948d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5948d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5948d-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5948d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5948d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5948d-132">INPUTS</span></span>

### <span data-ttu-id="5948d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="5948d-133">System.String</span></span>

### <span data-ttu-id="5948d-134">PSSecurityContact 中的 SecurityContacts （Security..。</span><span class="sxs-lookup"><span data-stu-id="5948d-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="5948d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5948d-135">OUTPUTS</span></span>

### <span data-ttu-id="5948d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5948d-136">System.Boolean</span></span>

## <span data-ttu-id="5948d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5948d-137">NOTES</span></span>

## <span data-ttu-id="5948d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5948d-138">RELATED LINKS</span></span>