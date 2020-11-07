---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 480c0a8e932b672542595983f33fd19bab6fec3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795713"
---
# <span data-ttu-id="cbe39-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="cbe39-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="cbe39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbe39-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe39-103">為裝置建立新使用者。</span><span class="sxs-lookup"><span data-stu-id="cbe39-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="cbe39-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbe39-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe39-105">說明</span><span class="sxs-lookup"><span data-stu-id="cbe39-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe39-106">**新的-AzDataBoxEdgeUser** Cmdlet 會為數據盒 Edge 裝置建立新的使用者。</span><span class="sxs-lookup"><span data-stu-id="cbe39-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="cbe39-107">只支援建立 type 類型的使用者 `Share` 。</span><span class="sxs-lookup"><span data-stu-id="cbe39-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="cbe39-108">示例</span><span class="sxs-lookup"><span data-stu-id="cbe39-108">EXAMPLES</span></span>

### <span data-ttu-id="cbe39-109">範例1</span><span class="sxs-lookup"><span data-stu-id="cbe39-109">Example 1</span></span>
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

## <span data-ttu-id="cbe39-110">參數</span><span class="sxs-lookup"><span data-stu-id="cbe39-110">PARAMETERS</span></span>

### <span data-ttu-id="cbe39-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbe39-111">-AsJob</span></span>
<span data-ttu-id="cbe39-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbe39-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbe39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe39-113">-DefaultProfile</span></span>
<span data-ttu-id="cbe39-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbe39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe39-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cbe39-115">-DeviceName</span></span>
<span data-ttu-id="cbe39-116">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="cbe39-116">Device Name</span></span>

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

### <span data-ttu-id="cbe39-117">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="cbe39-117">-EncryptionKey</span></span>
<span data-ttu-id="cbe39-118">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="cbe39-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="cbe39-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbe39-119">-Name</span></span>
<span data-ttu-id="cbe39-120">Username</span><span class="sxs-lookup"><span data-stu-id="cbe39-120">Username</span></span>

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

### <span data-ttu-id="cbe39-121">-Password</span><span class="sxs-lookup"><span data-stu-id="cbe39-121">-Password</span></span>
<span data-ttu-id="cbe39-122">密碼，提供成安全的字串</span><span class="sxs-lookup"><span data-stu-id="cbe39-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="cbe39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe39-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbe39-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cbe39-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cbe39-125">-類型</span><span class="sxs-lookup"><span data-stu-id="cbe39-125">-Type</span></span>
<span data-ttu-id="cbe39-126">選取 [UserType]</span><span class="sxs-lookup"><span data-stu-id="cbe39-126">Select UserType</span></span>

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

### <span data-ttu-id="cbe39-127">-確認</span><span class="sxs-lookup"><span data-stu-id="cbe39-127">-Confirm</span></span>
<span data-ttu-id="cbe39-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbe39-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe39-129">-WhatIf</span></span>
<span data-ttu-id="cbe39-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbe39-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbe39-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbe39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe39-132">CommonParameters</span></span>
<span data-ttu-id="cbe39-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbe39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe39-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cbe39-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe39-135">輸入</span><span class="sxs-lookup"><span data-stu-id="cbe39-135">INPUTS</span></span>

### <span data-ttu-id="cbe39-136">所有</span><span class="sxs-lookup"><span data-stu-id="cbe39-136">None</span></span>

## <span data-ttu-id="cbe39-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cbe39-137">OUTPUTS</span></span>

### <span data-ttu-id="cbe39-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cbe39-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="cbe39-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cbe39-139">NOTES</span></span>

## <span data-ttu-id="cbe39-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbe39-140">RELATED LINKS</span></span>
