---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: cd904a913ce9ea0cdcc2d347463fa21ac7e13943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915757"
---
# <span data-ttu-id="f541f-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f541f-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="f541f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f541f-102">SYNOPSIS</span></span>
<span data-ttu-id="f541f-103">為裝置建立新使用者。</span><span class="sxs-lookup"><span data-stu-id="f541f-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="f541f-104">語法</span><span class="sxs-lookup"><span data-stu-id="f541f-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f541f-105">描述</span><span class="sxs-lookup"><span data-stu-id="f541f-105">DESCRIPTION</span></span>
<span data-ttu-id="f541f-106">**New-AzStackEdgeUser** Cmdlet 會為 Stack Edge 裝置建立新使用者。</span><span class="sxs-lookup"><span data-stu-id="f541f-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="f541f-107">僅支援建立類型 `Share` 使用者。</span><span class="sxs-lookup"><span data-stu-id="f541f-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="f541f-108">例子</span><span class="sxs-lookup"><span data-stu-id="f541f-108">EXAMPLES</span></span>

### <span data-ttu-id="f541f-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="f541f-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="f541f-110">參數</span><span class="sxs-lookup"><span data-stu-id="f541f-110">PARAMETERS</span></span>

### <span data-ttu-id="f541f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f541f-111">-AsJob</span></span>
<span data-ttu-id="f541f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f541f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f541f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f541f-113">-DefaultProfile</span></span>
<span data-ttu-id="f541f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f541f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f541f-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f541f-115">-DeviceName</span></span>
<span data-ttu-id="f541f-116">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="f541f-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f541f-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f541f-117">-EncryptionKey</span></span>
<span data-ttu-id="f541f-118">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="f541f-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="f541f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f541f-119">-Name</span></span>
<span data-ttu-id="f541f-120">使用者</span><span class="sxs-lookup"><span data-stu-id="f541f-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f541f-121">-密碼</span><span class="sxs-lookup"><span data-stu-id="f541f-121">-Password</span></span>
<span data-ttu-id="f541f-122">密碼，以安全字串形式提供</span><span class="sxs-lookup"><span data-stu-id="f541f-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="f541f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f541f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f541f-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="f541f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f541f-125">-類型</span><span class="sxs-lookup"><span data-stu-id="f541f-125">-Type</span></span>
<span data-ttu-id="f541f-126">選取 UserType</span><span class="sxs-lookup"><span data-stu-id="f541f-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f541f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f541f-127">-Confirm</span></span>
<span data-ttu-id="f541f-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f541f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f541f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f541f-129">-WhatIf</span></span>
<span data-ttu-id="f541f-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f541f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f541f-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f541f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f541f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f541f-132">CommonParameters</span></span>
<span data-ttu-id="f541f-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f541f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f541f-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f541f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f541f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f541f-135">INPUTS</span></span>

### <span data-ttu-id="f541f-136">沒有</span><span class="sxs-lookup"><span data-stu-id="f541f-136">None</span></span>

## <span data-ttu-id="f541f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f541f-137">OUTPUTS</span></span>

### <span data-ttu-id="f541f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f541f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f541f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f541f-139">NOTES</span></span>

## <span data-ttu-id="f541f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f541f-140">RELATED LINKS</span></span>
