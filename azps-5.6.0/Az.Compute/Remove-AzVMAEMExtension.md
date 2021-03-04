---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 71fcf62049cfb15e830b4c8c5f311c042de55bb9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903313"
---
# <span data-ttu-id="3b894-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3b894-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="3b894-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b894-102">SYNOPSIS</span></span>
<span data-ttu-id="3b894-103">從虛擬機器移除 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3b894-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="3b894-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b894-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b894-105">描述</span><span class="sxs-lookup"><span data-stu-id="3b894-105">DESCRIPTION</span></span>
<span data-ttu-id="3b894-106">**Remove-AzVMAEMExtension** Cmdlet 會從虛擬機器 (AEM) Azure 增強型監控功能。</span><span class="sxs-lookup"><span data-stu-id="3b894-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="3b894-107">例子</span><span class="sxs-lookup"><span data-stu-id="3b894-107">EXAMPLES</span></span>

### <span data-ttu-id="3b894-108">範例 1：移除 AEM 擴充功能</span><span class="sxs-lookup"><span data-stu-id="3b894-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="3b894-109">此命令會移除名為 contoso-server 之虛擬機器的 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3b894-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="3b894-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b894-110">PARAMETERS</span></span>

### <span data-ttu-id="3b894-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b894-111">-DefaultProfile</span></span>
<span data-ttu-id="3b894-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b894-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b894-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b894-113">-Name</span></span>
<span data-ttu-id="3b894-114">指定此 Cmdlet 會移除 AEM 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="3b894-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b894-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b894-115">-NoWait</span></span>
<span data-ttu-id="3b894-116">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="3b894-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3b894-117">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="3b894-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3b894-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="3b894-118">-OSType</span></span>
<span data-ttu-id="3b894-119">指定作業系統磁片的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="3b894-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="3b894-120">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3b894-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="3b894-121">此參數可接受的值為：Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="3b894-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b894-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b894-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b894-123">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3b894-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="3b894-124">此 Cmdlet 會從該虛擬機器移除 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3b894-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="3b894-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="3b894-125">-VMName</span></span>
<span data-ttu-id="3b894-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b894-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3b894-127">此 Cmdlet 會移除此參數指定之虛擬機器的 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3b894-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b894-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b894-128">CommonParameters</span></span>
<span data-ttu-id="3b894-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b894-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b894-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b894-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b894-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3b894-131">INPUTS</span></span>

### <span data-ttu-id="3b894-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3b894-132">System.String</span></span>

## <span data-ttu-id="3b894-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3b894-133">OUTPUTS</span></span>

### <span data-ttu-id="3b894-134">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3b894-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3b894-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3b894-135">NOTES</span></span>

## <span data-ttu-id="3b894-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b894-136">RELATED LINKS</span></span>

[<span data-ttu-id="3b894-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3b894-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="3b894-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3b894-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="3b894-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3b894-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


