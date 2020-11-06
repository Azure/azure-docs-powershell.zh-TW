---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: b0387d10950073c4655c6e6015edc6957ae14edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449613"
---
# <span data-ttu-id="98fff-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98fff-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="98fff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98fff-102">SYNOPSIS</span></span>
<span data-ttu-id="98fff-103">移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="98fff-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98fff-104">句法</span><span class="sxs-lookup"><span data-stu-id="98fff-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98fff-105">說明</span><span class="sxs-lookup"><span data-stu-id="98fff-105">DESCRIPTION</span></span>
<span data-ttu-id="98fff-106">**AzureRmApplicationSecurityGroup** Cmdlet 會移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="98fff-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="98fff-107">示例</span><span class="sxs-lookup"><span data-stu-id="98fff-107">EXAMPLES</span></span>

### <span data-ttu-id="98fff-108">範例1</span><span class="sxs-lookup"><span data-stu-id="98fff-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="98fff-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyApplicationSecurityGrouo 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="98fff-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="98fff-110">參數</span><span class="sxs-lookup"><span data-stu-id="98fff-110">PARAMETERS</span></span>

### <span data-ttu-id="98fff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fff-111">-DefaultProfile</span></span>
<span data-ttu-id="98fff-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98fff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fff-113">-Force</span><span class="sxs-lookup"><span data-stu-id="98fff-113">-Force</span></span>
<span data-ttu-id="98fff-114">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="98fff-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="98fff-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="98fff-115">-Name</span></span>
<span data-ttu-id="98fff-116">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98fff-116">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fff-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98fff-117">-PassThru</span></span>
<span data-ttu-id="98fff-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="98fff-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="98fff-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="98fff-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98fff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fff-120">-ResourceGroupName</span></span>
<span data-ttu-id="98fff-121">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="98fff-121">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fff-122">-確認</span><span class="sxs-lookup"><span data-stu-id="98fff-122">-Confirm</span></span>
<span data-ttu-id="98fff-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98fff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98fff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98fff-124">-WhatIf</span></span>
<span data-ttu-id="98fff-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98fff-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98fff-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98fff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98fff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fff-127">CommonParameters</span></span>
<span data-ttu-id="98fff-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98fff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fff-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98fff-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fff-130">輸入</span><span class="sxs-lookup"><span data-stu-id="98fff-130">INPUTS</span></span>

### <span data-ttu-id="98fff-131">System.object</span><span class="sxs-lookup"><span data-stu-id="98fff-131">System.String</span></span>

## <span data-ttu-id="98fff-132">輸出</span><span class="sxs-lookup"><span data-stu-id="98fff-132">OUTPUTS</span></span>

### <span data-ttu-id="98fff-133">System.object</span><span class="sxs-lookup"><span data-stu-id="98fff-133">System.Object</span></span>

## <span data-ttu-id="98fff-134">筆記</span><span class="sxs-lookup"><span data-stu-id="98fff-134">NOTES</span></span>

## <span data-ttu-id="98fff-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="98fff-135">RELATED LINKS</span></span>

[<span data-ttu-id="98fff-136">新-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98fff-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="98fff-137">AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98fff-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
