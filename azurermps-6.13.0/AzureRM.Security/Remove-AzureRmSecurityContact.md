---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452723"
---
# <span data-ttu-id="b0038-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="b0038-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="b0038-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0038-102">SYNOPSIS</span></span>
<span data-ttu-id="b0038-103">刪除安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="b0038-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0038-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0038-104">SYNTAX</span></span>

### <span data-ttu-id="b0038-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b0038-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0038-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0038-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0038-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0038-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0038-108">說明</span><span class="sxs-lookup"><span data-stu-id="b0038-108">DESCRIPTION</span></span>
<span data-ttu-id="b0038-109">刪除安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="b0038-109">Deletes a security contact.</span></span>

## <span data-ttu-id="b0038-110">示例</span><span class="sxs-lookup"><span data-stu-id="b0038-110">EXAMPLES</span></span>

### <span data-ttu-id="b0038-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b0038-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="b0038-112">刪除「default1」安全連絡人</span><span class="sxs-lookup"><span data-stu-id="b0038-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="b0038-113">參數</span><span class="sxs-lookup"><span data-stu-id="b0038-113">PARAMETERS</span></span>

### <span data-ttu-id="b0038-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0038-114">-DefaultProfile</span></span>
<span data-ttu-id="b0038-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0038-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0038-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0038-116">-InputObject</span></span>
<span data-ttu-id="b0038-117">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b0038-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0038-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0038-118">-Name</span></span>
<span data-ttu-id="b0038-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b0038-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0038-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0038-120">-PassThru</span></span>
<span data-ttu-id="b0038-121">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="b0038-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b0038-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0038-122">-ResourceId</span></span>
<span data-ttu-id="b0038-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b0038-123">Resource ID.</span></span>

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

### <span data-ttu-id="b0038-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b0038-124">-Confirm</span></span>
<span data-ttu-id="b0038-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0038-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0038-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0038-126">-WhatIf</span></span>
<span data-ttu-id="b0038-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0038-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0038-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0038-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0038-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0038-129">CommonParameters</span></span>
<span data-ttu-id="b0038-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0038-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0038-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0038-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0038-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b0038-132">INPUTS</span></span>

### <span data-ttu-id="b0038-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b0038-133">System.String</span></span>
<span data-ttu-id="b0038-134">PSRemoveSecurityContactInputObject 中的 SecurityContacts （）</span><span class="sxs-lookup"><span data-stu-id="b0038-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="b0038-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b0038-135">OUTPUTS</span></span>

### <span data-ttu-id="b0038-136">PSSecurityContact 中的 SecurityContacts （Security..。</span><span class="sxs-lookup"><span data-stu-id="b0038-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="b0038-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b0038-137">NOTES</span></span>

## <span data-ttu-id="b0038-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0038-138">RELATED LINKS</span></span>
