---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622720"
---
# <span data-ttu-id="fcae2-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fcae2-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="fcae2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fcae2-102">SYNOPSIS</span></span>
<span data-ttu-id="fcae2-103">從虛擬機器移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="fcae2-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="fcae2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fcae2-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcae2-105">說明</span><span class="sxs-lookup"><span data-stu-id="fcae2-105">DESCRIPTION</span></span>
<span data-ttu-id="fcae2-106">**AzVMSqlServerExtension** Cmdlet 會從虛擬機器中移除 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="fcae2-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="fcae2-107">示例</span><span class="sxs-lookup"><span data-stu-id="fcae2-107">EXAMPLES</span></span>

### <span data-ttu-id="fcae2-108">範例1：移除 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="fcae2-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="fcae2-109">這個命令會從名為 ContosoVM22 的虛擬機器中移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="fcae2-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="fcae2-110">參數</span><span class="sxs-lookup"><span data-stu-id="fcae2-110">PARAMETERS</span></span>

### <span data-ttu-id="fcae2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcae2-111">-DefaultProfile</span></span>
<span data-ttu-id="fcae2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcae2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcae2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="fcae2-113">-Name</span></span>
<span data-ttu-id="fcae2-114">指定此 Cmdlet 移除之副檔名之 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcae2-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fcae2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcae2-115">-ResourceGroupName</span></span>
<span data-ttu-id="fcae2-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcae2-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fcae2-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="fcae2-117">-VMName</span></span>
<span data-ttu-id="fcae2-118">指定此 Cmdlet 從中移除 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="fcae2-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="fcae2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcae2-119">CommonParameters</span></span>
<span data-ttu-id="fcae2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fcae2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcae2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fcae2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcae2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fcae2-122">INPUTS</span></span>

### <span data-ttu-id="fcae2-123">System.object</span><span class="sxs-lookup"><span data-stu-id="fcae2-123">System.String</span></span>

## <span data-ttu-id="fcae2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fcae2-124">OUTPUTS</span></span>

### <span data-ttu-id="fcae2-125">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="fcae2-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fcae2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fcae2-126">NOTES</span></span>

## <span data-ttu-id="fcae2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcae2-127">RELATED LINKS</span></span>

[<span data-ttu-id="fcae2-128">AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fcae2-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="fcae2-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fcae2-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


