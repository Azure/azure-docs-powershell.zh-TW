---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 6abc37d37bf06025389329b8b917db8a75cefd1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911713"
---
# <span data-ttu-id="9671c-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9671c-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="9671c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9671c-102">SYNOPSIS</span></span>
<span data-ttu-id="9671c-103">為裝置建立新使用者。</span><span class="sxs-lookup"><span data-stu-id="9671c-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="9671c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9671c-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9671c-105">描述</span><span class="sxs-lookup"><span data-stu-id="9671c-105">DESCRIPTION</span></span>
<span data-ttu-id="9671c-106">**New-AzDataBoxEdgeUser** Cmdlet 會為 Data Box Edge 裝置建立新使用者。</span><span class="sxs-lookup"><span data-stu-id="9671c-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="9671c-107">僅支援建立類型 `Share` 使用者。</span><span class="sxs-lookup"><span data-stu-id="9671c-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="9671c-108">例子</span><span class="sxs-lookup"><span data-stu-id="9671c-108">EXAMPLES</span></span>

### <span data-ttu-id="9671c-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="9671c-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="9671c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9671c-110">PARAMETERS</span></span>

### <span data-ttu-id="9671c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9671c-111">-AsJob</span></span>
<span data-ttu-id="9671c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9671c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9671c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9671c-113">-DefaultProfile</span></span>
<span data-ttu-id="9671c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9671c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9671c-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9671c-115">-DeviceName</span></span>
<span data-ttu-id="9671c-116">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="9671c-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9671c-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9671c-117">-EncryptionKey</span></span>
<span data-ttu-id="9671c-118">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="9671c-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9671c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9671c-119">-Name</span></span>
<span data-ttu-id="9671c-120">使用者</span><span class="sxs-lookup"><span data-stu-id="9671c-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9671c-121">-密碼</span><span class="sxs-lookup"><span data-stu-id="9671c-121">-Password</span></span>
<span data-ttu-id="9671c-122">密碼，以安全字串形式提供</span><span class="sxs-lookup"><span data-stu-id="9671c-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="9671c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9671c-123">-ResourceGroupName</span></span>
<span data-ttu-id="9671c-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="9671c-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9671c-125">-類型</span><span class="sxs-lookup"><span data-stu-id="9671c-125">-Type</span></span>
<span data-ttu-id="9671c-126">選取 UserType</span><span class="sxs-lookup"><span data-stu-id="9671c-126">Select UserType</span></span>

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

### <span data-ttu-id="9671c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="9671c-127">-Confirm</span></span>
<span data-ttu-id="9671c-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9671c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9671c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9671c-129">-WhatIf</span></span>
<span data-ttu-id="9671c-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9671c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9671c-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9671c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9671c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9671c-132">CommonParameters</span></span>
<span data-ttu-id="9671c-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9671c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9671c-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9671c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9671c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9671c-135">INPUTS</span></span>

### <span data-ttu-id="9671c-136">沒有</span><span class="sxs-lookup"><span data-stu-id="9671c-136">None</span></span>

## <span data-ttu-id="9671c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9671c-137">OUTPUTS</span></span>

### <span data-ttu-id="9671c-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9671c-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9671c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9671c-139">NOTES</span></span>

## <span data-ttu-id="9671c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9671c-140">RELATED LINKS</span></span>
