---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287707"
---
# <span data-ttu-id="778b8-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="778b8-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="778b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="778b8-102">SYNOPSIS</span></span>
<span data-ttu-id="778b8-103">為裝置建立新使用者。</span><span class="sxs-lookup"><span data-stu-id="778b8-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="778b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="778b8-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="778b8-105">DESCRIPTION</span></span>
<span data-ttu-id="778b8-106">**新的-AzStackEdgeUser** Cmdlet 會針對堆疊 Edge 裝置建立新的使用者。</span><span class="sxs-lookup"><span data-stu-id="778b8-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="778b8-107">只支援建立 type 類型的使用者 `Share` 。</span><span class="sxs-lookup"><span data-stu-id="778b8-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="778b8-108">示例</span><span class="sxs-lookup"><span data-stu-id="778b8-108">EXAMPLES</span></span>

### <span data-ttu-id="778b8-109">範例1</span><span class="sxs-lookup"><span data-stu-id="778b8-109">Example 1</span></span>
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

## <span data-ttu-id="778b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="778b8-110">PARAMETERS</span></span>

### <span data-ttu-id="778b8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="778b8-111">-AsJob</span></span>
<span data-ttu-id="778b8-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="778b8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="778b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778b8-113">-DefaultProfile</span></span>
<span data-ttu-id="778b8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="778b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="778b8-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="778b8-115">-DeviceName</span></span>
<span data-ttu-id="778b8-116">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="778b8-116">Device Name</span></span>

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

### <span data-ttu-id="778b8-117">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="778b8-117">-EncryptionKey</span></span>
<span data-ttu-id="778b8-118">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="778b8-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="778b8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="778b8-119">-Name</span></span>
<span data-ttu-id="778b8-120">Username</span><span class="sxs-lookup"><span data-stu-id="778b8-120">Username</span></span>

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

### <span data-ttu-id="778b8-121">-Password</span><span class="sxs-lookup"><span data-stu-id="778b8-121">-Password</span></span>
<span data-ttu-id="778b8-122">密碼，提供成安全的字串</span><span class="sxs-lookup"><span data-stu-id="778b8-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="778b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="778b8-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="778b8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="778b8-125">-類型</span><span class="sxs-lookup"><span data-stu-id="778b8-125">-Type</span></span>
<span data-ttu-id="778b8-126">選取 [UserType]</span><span class="sxs-lookup"><span data-stu-id="778b8-126">Select UserType</span></span>

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

### <span data-ttu-id="778b8-127">-確認</span><span class="sxs-lookup"><span data-stu-id="778b8-127">-Confirm</span></span>
<span data-ttu-id="778b8-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="778b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778b8-129">-WhatIf</span></span>
<span data-ttu-id="778b8-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="778b8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="778b8-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="778b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778b8-132">CommonParameters</span></span>
<span data-ttu-id="778b8-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="778b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778b8-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="778b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778b8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="778b8-135">INPUTS</span></span>

### <span data-ttu-id="778b8-136">所有</span><span class="sxs-lookup"><span data-stu-id="778b8-136">None</span></span>

## <span data-ttu-id="778b8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="778b8-137">OUTPUTS</span></span>

### <span data-ttu-id="778b8-138">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="778b8-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="778b8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="778b8-139">NOTES</span></span>

## <span data-ttu-id="778b8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="778b8-140">RELATED LINKS</span></span>
