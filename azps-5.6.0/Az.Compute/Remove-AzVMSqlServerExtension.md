---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 42fb10ef388fdda9616f78453163db822da9d036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910258"
---
# <span data-ttu-id="d750b-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d750b-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="d750b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d750b-102">SYNOPSIS</span></span>
<span data-ttu-id="d750b-103">從虛擬機器移除 SQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d750b-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="d750b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d750b-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d750b-105">描述</span><span class="sxs-lookup"><span data-stu-id="d750b-105">DESCRIPTION</span></span>
<span data-ttu-id="d750b-106">**Remove-AzCMSqlServerExtension** Cmdlet 會從虛擬機器移除 AzureSQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d750b-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="d750b-107">例子</span><span class="sxs-lookup"><span data-stu-id="d750b-107">EXAMPLES</span></span>

### <span data-ttu-id="d750b-108">範例 1：移除 SQL Server 擴充功能</span><span class="sxs-lookup"><span data-stu-id="d750b-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="d750b-109">此命令會從名為 Contoso VIRTUAL22 的虛擬機器移除 SQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d750b-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="d750b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d750b-110">PARAMETERS</span></span>

### <span data-ttu-id="d750b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d750b-111">-DefaultProfile</span></span>
<span data-ttu-id="d750b-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d750b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d750b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d750b-113">-Name</span></span>
<span data-ttu-id="d750b-114">指定此 Cmdlet 移除的擴充功能 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="d750b-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d750b-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d750b-115">-NoWait</span></span>
<span data-ttu-id="d750b-116">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="d750b-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d750b-117">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="d750b-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d750b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d750b-118">-ResourceGroupName</span></span>
<span data-ttu-id="d750b-119">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d750b-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d750b-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="d750b-120">-VMName</span></span>
<span data-ttu-id="d750b-121">指定此 Cmdlet 會移除 SQL Server 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="d750b-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="d750b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d750b-122">CommonParameters</span></span>
<span data-ttu-id="d750b-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d750b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d750b-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d750b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d750b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d750b-125">INPUTS</span></span>

### <span data-ttu-id="d750b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d750b-126">System.String</span></span>

## <span data-ttu-id="d750b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="d750b-127">OUTPUTS</span></span>

### <span data-ttu-id="d750b-128">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d750b-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d750b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d750b-129">NOTES</span></span>

## <span data-ttu-id="d750b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d750b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d750b-131">Get-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d750b-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="d750b-132">Set-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d750b-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


