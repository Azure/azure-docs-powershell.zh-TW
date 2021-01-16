---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280184"
---
# <span data-ttu-id="bdfc8-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bdfc8-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="bdfc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdfc8-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfc8-103">為裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="bdfc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdfc8-104">SYNTAX</span></span>

### <span data-ttu-id="bdfc8-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bdfc8-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdfc8-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdfc8-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdfc8-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdfc8-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdfc8-108">說明</span><span class="sxs-lookup"><span data-stu-id="bdfc8-108">DESCRIPTION</span></span>
<span data-ttu-id="bdfc8-109">**AzStackEdgeUser** Cmdlet 會針對堆疊 Edge 裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="bdfc8-110">示例</span><span class="sxs-lookup"><span data-stu-id="bdfc8-110">EXAMPLES</span></span>

### <span data-ttu-id="bdfc8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bdfc8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="bdfc8-112">參數</span><span class="sxs-lookup"><span data-stu-id="bdfc8-112">PARAMETERS</span></span>

### <span data-ttu-id="bdfc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdfc8-113">-AsJob</span></span>
<span data-ttu-id="bdfc8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bdfc8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdfc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfc8-115">-DefaultProfile</span></span>
<span data-ttu-id="bdfc8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdfc8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bdfc8-117">-DeviceName</span></span>
<span data-ttu-id="bdfc8-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="bdfc8-118">Device Name</span></span>

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

### <span data-ttu-id="bdfc8-119">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="bdfc8-119">-EncryptionKey</span></span>
<span data-ttu-id="bdfc8-120">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="bdfc8-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="bdfc8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdfc8-121">-InputObject</span></span>
<span data-ttu-id="bdfc8-122">輸入物件</span><span class="sxs-lookup"><span data-stu-id="bdfc8-122">Input Object</span></span>

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

### <span data-ttu-id="bdfc8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdfc8-123">-Name</span></span>
<span data-ttu-id="bdfc8-124">Username</span><span class="sxs-lookup"><span data-stu-id="bdfc8-124">Username</span></span>

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

### <span data-ttu-id="bdfc8-125">-Password</span><span class="sxs-lookup"><span data-stu-id="bdfc8-125">-Password</span></span>
<span data-ttu-id="bdfc8-126">密碼，提供成安全的字串</span><span class="sxs-lookup"><span data-stu-id="bdfc8-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="bdfc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdfc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="bdfc8-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bdfc8-128">Resource Group Name</span></span>

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

### <span data-ttu-id="bdfc8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdfc8-129">-ResourceId</span></span>
<span data-ttu-id="bdfc8-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdfc8-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="bdfc8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bdfc8-131">-Confirm</span></span>
<span data-ttu-id="bdfc8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdfc8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdfc8-133">-WhatIf</span></span>
<span data-ttu-id="bdfc8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdfc8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdfc8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfc8-136">CommonParameters</span></span>
<span data-ttu-id="bdfc8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfc8-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bdfc8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfc8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bdfc8-139">INPUTS</span></span>

### <span data-ttu-id="bdfc8-140">所有</span><span class="sxs-lookup"><span data-stu-id="bdfc8-140">None</span></span>

## <span data-ttu-id="bdfc8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bdfc8-141">OUTPUTS</span></span>

### <span data-ttu-id="bdfc8-142">PSStackEdgeUser （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="bdfc8-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="bdfc8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bdfc8-143">NOTES</span></span>

## <span data-ttu-id="bdfc8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdfc8-144">RELATED LINKS</span></span>
