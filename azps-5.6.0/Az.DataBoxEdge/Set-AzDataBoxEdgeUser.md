---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: a2de03f28935fb8002966e0e9251218809ddec5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906741"
---
# <span data-ttu-id="70dc8-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="70dc8-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="70dc8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="70dc8-103">為裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="70dc8-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="70dc8-104">語法</span><span class="sxs-lookup"><span data-stu-id="70dc8-104">SYNTAX</span></span>

### <span data-ttu-id="70dc8-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="70dc8-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70dc8-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70dc8-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70dc8-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70dc8-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70dc8-108">描述</span><span class="sxs-lookup"><span data-stu-id="70dc8-108">DESCRIPTION</span></span>
<span data-ttu-id="70dc8-109">**Set-AzDataBoxEdgeUser** Cmdlet 會為 Data Box Edge 裝置上的使用者設定新密碼。</span><span class="sxs-lookup"><span data-stu-id="70dc8-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="70dc8-110">例子</span><span class="sxs-lookup"><span data-stu-id="70dc8-110">EXAMPLES</span></span>

### <span data-ttu-id="70dc8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="70dc8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="70dc8-112">參數</span><span class="sxs-lookup"><span data-stu-id="70dc8-112">PARAMETERS</span></span>

### <span data-ttu-id="70dc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70dc8-113">-AsJob</span></span>
<span data-ttu-id="70dc8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70dc8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70dc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70dc8-115">-DefaultProfile</span></span>
<span data-ttu-id="70dc8-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70dc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70dc8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="70dc8-117">-DeviceName</span></span>
<span data-ttu-id="70dc8-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="70dc8-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dc8-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="70dc8-119">-EncryptionKey</span></span>
<span data-ttu-id="70dc8-120">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="70dc8-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="70dc8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70dc8-121">-InputObject</span></span>
<span data-ttu-id="70dc8-122">輸入物件</span><span class="sxs-lookup"><span data-stu-id="70dc8-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dc8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="70dc8-123">-Name</span></span>
<span data-ttu-id="70dc8-124">使用者</span><span class="sxs-lookup"><span data-stu-id="70dc8-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dc8-125">-密碼</span><span class="sxs-lookup"><span data-stu-id="70dc8-125">-Password</span></span>
<span data-ttu-id="70dc8-126">密碼，以安全字串形式提供</span><span class="sxs-lookup"><span data-stu-id="70dc8-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="70dc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70dc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="70dc8-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="70dc8-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dc8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70dc8-129">-ResourceId</span></span>
<span data-ttu-id="70dc8-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="70dc8-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70dc8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="70dc8-131">-Confirm</span></span>
<span data-ttu-id="70dc8-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="70dc8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70dc8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70dc8-133">-WhatIf</span></span>
<span data-ttu-id="70dc8-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70dc8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70dc8-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70dc8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70dc8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70dc8-136">CommonParameters</span></span>
<span data-ttu-id="70dc8-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70dc8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70dc8-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70dc8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70dc8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="70dc8-139">INPUTS</span></span>

### <span data-ttu-id="70dc8-140">沒有</span><span class="sxs-lookup"><span data-stu-id="70dc8-140">None</span></span>

## <span data-ttu-id="70dc8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="70dc8-141">OUTPUTS</span></span>

### <span data-ttu-id="70dc8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="70dc8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="70dc8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="70dc8-143">NOTES</span></span>

## <span data-ttu-id="70dc8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="70dc8-144">RELATED LINKS</span></span>
