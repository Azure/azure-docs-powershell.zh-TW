---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970982"
---
# <span data-ttu-id="f7207-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f7207-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="f7207-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7207-102">SYNOPSIS</span></span>
<span data-ttu-id="f7207-103">在 (ANF) 帳戶] 中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="f7207-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="f7207-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7207-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7207-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7207-105">DESCRIPTION</span></span>
<span data-ttu-id="f7207-106">**新的-AzNetAppFilesAccount** Cmdlet 會建立 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f7207-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="f7207-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7207-107">EXAMPLES</span></span>

### <span data-ttu-id="f7207-108">範例1：建立 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="f7207-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="f7207-109">這個命令會建立新的 ANF 帳戶 "MyAnfAccount"。</span><span class="sxs-lookup"><span data-stu-id="f7207-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="f7207-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7207-110">PARAMETERS</span></span>

### <span data-ttu-id="f7207-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f7207-111">-ActiveDirectory</span></span>
<span data-ttu-id="f7207-112">代表活動目錄的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="f7207-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7207-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7207-113">-DefaultProfile</span></span>
<span data-ttu-id="f7207-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7207-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7207-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f7207-115">-Location</span></span>
<span data-ttu-id="f7207-116">資源的位置</span><span class="sxs-lookup"><span data-stu-id="f7207-116">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7207-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7207-117">-Name</span></span>
<span data-ttu-id="f7207-118">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="f7207-118">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7207-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7207-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7207-120">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="f7207-120">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7207-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7207-121">-Tag</span></span>
<span data-ttu-id="f7207-122">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="f7207-122">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7207-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f7207-123">-Confirm</span></span>
<span data-ttu-id="f7207-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7207-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7207-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7207-125">-WhatIf</span></span>
<span data-ttu-id="f7207-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7207-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7207-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7207-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7207-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7207-128">CommonParameters</span></span>
<span data-ttu-id="f7207-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7207-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7207-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f7207-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7207-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f7207-131">INPUTS</span></span>

### <span data-ttu-id="f7207-132">所有</span><span class="sxs-lookup"><span data-stu-id="f7207-132">None</span></span>

## <span data-ttu-id="f7207-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f7207-133">OUTPUTS</span></span>

### <span data-ttu-id="f7207-134">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="f7207-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f7207-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f7207-135">NOTES</span></span>

## <span data-ttu-id="f7207-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7207-136">RELATED LINKS</span></span>
