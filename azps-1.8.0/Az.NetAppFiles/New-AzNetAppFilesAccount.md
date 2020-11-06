---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622222"
---
# <span data-ttu-id="6f8dc-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6f8dc-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="6f8dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8dc-103">在 (ANF) 帳戶] 中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="6f8dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f8dc-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8dc-106">**新的-AzNetAppFilesAccount** Cmdlet 會建立 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="6f8dc-107">示例</span><span class="sxs-lookup"><span data-stu-id="6f8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8dc-108">範例1：建立 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="6f8dc-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="6f8dc-109">這個命令會建立新的 ANF 帳戶 "MyAnfAccount"。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="6f8dc-110">參數</span><span class="sxs-lookup"><span data-stu-id="6f8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="6f8dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8dc-111">-DefaultProfile</span></span>
<span data-ttu-id="6f8dc-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8dc-113">-位置</span><span class="sxs-lookup"><span data-stu-id="6f8dc-113">-Location</span></span>
<span data-ttu-id="6f8dc-114">資源的位置</span><span class="sxs-lookup"><span data-stu-id="6f8dc-114">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8dc-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f8dc-115">-Name</span></span>
<span data-ttu-id="6f8dc-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="6f8dc-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f8dc-118">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="6f8dc-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8dc-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f8dc-119">-Tag</span></span>
<span data-ttu-id="6f8dc-120">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="6f8dc-120">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8dc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="6f8dc-121">-Confirm</span></span>
<span data-ttu-id="6f8dc-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8dc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8dc-123">-WhatIf</span></span>
<span data-ttu-id="6f8dc-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f8dc-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8dc-126">CommonParameters</span></span>
<span data-ttu-id="6f8dc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6f8dc-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8dc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6f8dc-129">INPUTS</span></span>

### <span data-ttu-id="6f8dc-130">所有</span><span class="sxs-lookup"><span data-stu-id="6f8dc-130">None</span></span>

## <span data-ttu-id="6f8dc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6f8dc-131">OUTPUTS</span></span>

### <span data-ttu-id="6f8dc-132">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6f8dc-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6f8dc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6f8dc-133">NOTES</span></span>

## <span data-ttu-id="6f8dc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f8dc-134">RELATED LINKS</span></span>