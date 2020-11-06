---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 81acbdd914d4a3cdb69da9ac0d2093f4e1dd4cdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613226"
---
# <span data-ttu-id="0dddb-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0dddb-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="0dddb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dddb-102">SYNOPSIS</span></span>
<span data-ttu-id="0dddb-103">從虛擬機器移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="0dddb-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="0dddb-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dddb-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dddb-105">說明</span><span class="sxs-lookup"><span data-stu-id="0dddb-105">DESCRIPTION</span></span>
<span data-ttu-id="0dddb-106">**AzVMSqlServerExtension** Cmdlet 會從虛擬機器中移除 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="0dddb-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="0dddb-107">示例</span><span class="sxs-lookup"><span data-stu-id="0dddb-107">EXAMPLES</span></span>

### <span data-ttu-id="0dddb-108">範例1：移除 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="0dddb-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="0dddb-109">這個命令會從名為 ContosoVM22 的虛擬機器中移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="0dddb-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="0dddb-110">參數</span><span class="sxs-lookup"><span data-stu-id="0dddb-110">PARAMETERS</span></span>

### <span data-ttu-id="0dddb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dddb-111">-DefaultProfile</span></span>
<span data-ttu-id="0dddb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dddb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dddb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dddb-113">-Name</span></span>
<span data-ttu-id="0dddb-114">指定此 Cmdlet 移除之副檔名之 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dddb-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0dddb-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0dddb-115">-NoWait</span></span>
<span data-ttu-id="0dddb-116">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="0dddb-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0dddb-117">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="0dddb-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0dddb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dddb-118">-ResourceGroupName</span></span>
<span data-ttu-id="0dddb-119">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dddb-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0dddb-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="0dddb-120">-VMName</span></span>
<span data-ttu-id="0dddb-121">指定此 Cmdlet 從中移除 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="0dddb-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="0dddb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dddb-122">CommonParameters</span></span>
<span data-ttu-id="0dddb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dddb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dddb-124">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0dddb-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dddb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0dddb-125">INPUTS</span></span>

### <span data-ttu-id="0dddb-126">System.object</span><span class="sxs-lookup"><span data-stu-id="0dddb-126">System.String</span></span>

## <span data-ttu-id="0dddb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0dddb-127">OUTPUTS</span></span>

### <span data-ttu-id="0dddb-128">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0dddb-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0dddb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0dddb-129">NOTES</span></span>

## <span data-ttu-id="0dddb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dddb-130">RELATED LINKS</span></span>

[<span data-ttu-id="0dddb-131">AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0dddb-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="0dddb-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0dddb-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


