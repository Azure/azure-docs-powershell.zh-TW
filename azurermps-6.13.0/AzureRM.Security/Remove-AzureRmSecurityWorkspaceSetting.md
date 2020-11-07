---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624027"
---
# <span data-ttu-id="161cf-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="161cf-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="161cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="161cf-102">SYNOPSIS</span></span>
<span data-ttu-id="161cf-103">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="161cf-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="161cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="161cf-104">SYNTAX</span></span>

### <span data-ttu-id="161cf-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="161cf-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="161cf-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="161cf-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="161cf-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="161cf-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="161cf-108">說明</span><span class="sxs-lookup"><span data-stu-id="161cf-108">DESCRIPTION</span></span>
<span data-ttu-id="161cf-109">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="161cf-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="161cf-110">這個動作會將新安裝的安全代理程式報告到這個 susbscription 的預設工作區。</span><span class="sxs-lookup"><span data-stu-id="161cf-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="161cf-111">示例</span><span class="sxs-lookup"><span data-stu-id="161cf-111">EXAMPLES</span></span>

### <span data-ttu-id="161cf-112">範例1</span><span class="sxs-lookup"><span data-stu-id="161cf-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="161cf-113">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="161cf-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="161cf-114">參數</span><span class="sxs-lookup"><span data-stu-id="161cf-114">PARAMETERS</span></span>

### <span data-ttu-id="161cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161cf-115">-DefaultProfile</span></span>
<span data-ttu-id="161cf-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="161cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="161cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="161cf-117">-InputObject</span></span>
<span data-ttu-id="161cf-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="161cf-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="161cf-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="161cf-119">-Name</span></span>
<span data-ttu-id="161cf-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="161cf-120">Resource name.</span></span>

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

### <span data-ttu-id="161cf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="161cf-121">-PassThru</span></span>
<span data-ttu-id="161cf-122">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="161cf-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="161cf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="161cf-123">-ResourceId</span></span>
<span data-ttu-id="161cf-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="161cf-124">Resource ID.</span></span>

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

### <span data-ttu-id="161cf-125">-確認</span><span class="sxs-lookup"><span data-stu-id="161cf-125">-Confirm</span></span>
<span data-ttu-id="161cf-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="161cf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="161cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="161cf-127">-WhatIf</span></span>
<span data-ttu-id="161cf-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="161cf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="161cf-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="161cf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="161cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161cf-130">CommonParameters</span></span>
<span data-ttu-id="161cf-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="161cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161cf-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="161cf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161cf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="161cf-133">INPUTS</span></span>

### <span data-ttu-id="161cf-134">System.object</span><span class="sxs-lookup"><span data-stu-id="161cf-134">System.String</span></span>
<span data-ttu-id="161cf-135">PSRemoveWorkspaceSettingInputObject 中的 WorkspaceSettings （）</span><span class="sxs-lookup"><span data-stu-id="161cf-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="161cf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="161cf-136">OUTPUTS</span></span>

### <span data-ttu-id="161cf-137">PSSecurityWorkspaceSetting 中的 WorkspaceSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="161cf-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="161cf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="161cf-138">NOTES</span></span>

## <span data-ttu-id="161cf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="161cf-139">RELATED LINKS</span></span>
