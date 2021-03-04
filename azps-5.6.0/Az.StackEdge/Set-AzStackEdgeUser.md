---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 0c3494e96290702c424a8e8bac7680daa376c488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913014"
---
# <span data-ttu-id="15fe3-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="15fe3-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="15fe3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="15fe3-103">為裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="15fe3-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="15fe3-104">語法</span><span class="sxs-lookup"><span data-stu-id="15fe3-104">SYNTAX</span></span>

### <span data-ttu-id="15fe3-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="15fe3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fe3-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15fe3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fe3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15fe3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15fe3-108">描述</span><span class="sxs-lookup"><span data-stu-id="15fe3-108">DESCRIPTION</span></span>
<span data-ttu-id="15fe3-109">**Set-AzStackEdgeUser** Cmdlet 會為 Stack Edge 裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="15fe3-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="15fe3-110">例子</span><span class="sxs-lookup"><span data-stu-id="15fe3-110">EXAMPLES</span></span>

### <span data-ttu-id="15fe3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="15fe3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="15fe3-112">參數</span><span class="sxs-lookup"><span data-stu-id="15fe3-112">PARAMETERS</span></span>

### <span data-ttu-id="15fe3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15fe3-113">-AsJob</span></span>
<span data-ttu-id="15fe3-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="15fe3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15fe3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fe3-115">-DefaultProfile</span></span>
<span data-ttu-id="15fe3-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15fe3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15fe3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="15fe3-117">-DeviceName</span></span>
<span data-ttu-id="15fe3-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="15fe3-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="15fe3-119">-EncryptionKey</span></span>
<span data-ttu-id="15fe3-120">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="15fe3-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15fe3-121">-InputObject</span></span>
<span data-ttu-id="15fe3-122">輸入物件</span><span class="sxs-lookup"><span data-stu-id="15fe3-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="15fe3-123">-Name</span></span>
<span data-ttu-id="15fe3-124">使用者</span><span class="sxs-lookup"><span data-stu-id="15fe3-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-125">-密碼</span><span class="sxs-lookup"><span data-stu-id="15fe3-125">-Password</span></span>
<span data-ttu-id="15fe3-126">密碼，以安全字串形式提供</span><span class="sxs-lookup"><span data-stu-id="15fe3-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fe3-127">-ResourceGroupName</span></span>
<span data-ttu-id="15fe3-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="15fe3-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15fe3-129">-ResourceId</span></span>
<span data-ttu-id="15fe3-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="15fe3-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fe3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="15fe3-131">-Confirm</span></span>
<span data-ttu-id="15fe3-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="15fe3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15fe3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15fe3-133">-WhatIf</span></span>
<span data-ttu-id="15fe3-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15fe3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15fe3-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15fe3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15fe3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fe3-136">CommonParameters</span></span>
<span data-ttu-id="15fe3-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15fe3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fe3-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15fe3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fe3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="15fe3-139">INPUTS</span></span>

### <span data-ttu-id="15fe3-140">沒有</span><span class="sxs-lookup"><span data-stu-id="15fe3-140">None</span></span>

## <span data-ttu-id="15fe3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="15fe3-141">OUTPUTS</span></span>

### <span data-ttu-id="15fe3-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="15fe3-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="15fe3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="15fe3-143">NOTES</span></span>

## <span data-ttu-id="15fe3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="15fe3-144">RELATED LINKS</span></span>
