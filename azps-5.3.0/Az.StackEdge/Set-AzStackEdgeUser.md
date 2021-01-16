---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285519"
---
# <span data-ttu-id="35885-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="35885-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="35885-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35885-102">SYNOPSIS</span></span>
<span data-ttu-id="35885-103">為裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="35885-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="35885-104">句法</span><span class="sxs-lookup"><span data-stu-id="35885-104">SYNTAX</span></span>

### <span data-ttu-id="35885-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="35885-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35885-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35885-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35885-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35885-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35885-108">說明</span><span class="sxs-lookup"><span data-stu-id="35885-108">DESCRIPTION</span></span>
<span data-ttu-id="35885-109">**AzStackEdgeUser** Cmdlet 會針對堆疊 Edge 裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="35885-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="35885-110">示例</span><span class="sxs-lookup"><span data-stu-id="35885-110">EXAMPLES</span></span>

### <span data-ttu-id="35885-111">範例1</span><span class="sxs-lookup"><span data-stu-id="35885-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="35885-112">參數</span><span class="sxs-lookup"><span data-stu-id="35885-112">PARAMETERS</span></span>

### <span data-ttu-id="35885-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35885-113">-AsJob</span></span>
<span data-ttu-id="35885-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="35885-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35885-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35885-115">-DefaultProfile</span></span>
<span data-ttu-id="35885-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35885-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35885-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="35885-117">-DeviceName</span></span>
<span data-ttu-id="35885-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="35885-118">Device Name</span></span>

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

### <span data-ttu-id="35885-119">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="35885-119">-EncryptionKey</span></span>
<span data-ttu-id="35885-120">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="35885-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="35885-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35885-121">-InputObject</span></span>
<span data-ttu-id="35885-122">輸入物件</span><span class="sxs-lookup"><span data-stu-id="35885-122">Input Object</span></span>

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

### <span data-ttu-id="35885-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="35885-123">-Name</span></span>
<span data-ttu-id="35885-124">Username</span><span class="sxs-lookup"><span data-stu-id="35885-124">Username</span></span>

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

### <span data-ttu-id="35885-125">-Password</span><span class="sxs-lookup"><span data-stu-id="35885-125">-Password</span></span>
<span data-ttu-id="35885-126">密碼，提供成安全的字串</span><span class="sxs-lookup"><span data-stu-id="35885-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="35885-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35885-127">-ResourceGroupName</span></span>
<span data-ttu-id="35885-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="35885-128">Resource Group Name</span></span>

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

### <span data-ttu-id="35885-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35885-129">-ResourceId</span></span>
<span data-ttu-id="35885-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="35885-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="35885-131">-確認</span><span class="sxs-lookup"><span data-stu-id="35885-131">-Confirm</span></span>
<span data-ttu-id="35885-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35885-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35885-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35885-133">-WhatIf</span></span>
<span data-ttu-id="35885-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35885-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35885-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35885-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35885-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35885-136">CommonParameters</span></span>
<span data-ttu-id="35885-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35885-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35885-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="35885-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35885-139">輸入</span><span class="sxs-lookup"><span data-stu-id="35885-139">INPUTS</span></span>

### <span data-ttu-id="35885-140">所有</span><span class="sxs-lookup"><span data-stu-id="35885-140">None</span></span>

## <span data-ttu-id="35885-141">輸出</span><span class="sxs-lookup"><span data-stu-id="35885-141">OUTPUTS</span></span>

### <span data-ttu-id="35885-142">PSStackEdgeUser （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="35885-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="35885-143">筆記</span><span class="sxs-lookup"><span data-stu-id="35885-143">NOTES</span></span>

## <span data-ttu-id="35885-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="35885-144">RELATED LINKS</span></span>
