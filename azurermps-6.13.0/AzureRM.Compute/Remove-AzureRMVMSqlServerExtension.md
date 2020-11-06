---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 83f697733d56ae7d99bc0b2660b5abbaca15a71f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456143"
---
# <span data-ttu-id="88741-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="88741-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="88741-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88741-102">SYNOPSIS</span></span>
<span data-ttu-id="88741-103">從虛擬機器移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="88741-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88741-104">句法</span><span class="sxs-lookup"><span data-stu-id="88741-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88741-105">說明</span><span class="sxs-lookup"><span data-stu-id="88741-105">DESCRIPTION</span></span>
<span data-ttu-id="88741-106">**AzureRmVMSqlServerExtension** Cmdlet 會從虛擬機器中移除 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="88741-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="88741-107">示例</span><span class="sxs-lookup"><span data-stu-id="88741-107">EXAMPLES</span></span>

### <span data-ttu-id="88741-108">範例1：移除 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="88741-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="88741-109">這個命令會從名為 ContosoVM22 的虛擬機器中移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="88741-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="88741-110">參數</span><span class="sxs-lookup"><span data-stu-id="88741-110">PARAMETERS</span></span>

### <span data-ttu-id="88741-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88741-111">-DefaultProfile</span></span>
<span data-ttu-id="88741-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88741-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88741-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="88741-113">-Name</span></span>
<span data-ttu-id="88741-114">指定此 Cmdlet 移除之副檔名之 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="88741-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88741-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88741-115">-ResourceGroupName</span></span>
<span data-ttu-id="88741-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88741-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="88741-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="88741-117">-VMName</span></span>
<span data-ttu-id="88741-118">指定此 Cmdlet 從中移除 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="88741-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="88741-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88741-119">CommonParameters</span></span>
<span data-ttu-id="88741-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88741-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88741-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88741-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88741-122">輸入</span><span class="sxs-lookup"><span data-stu-id="88741-122">INPUTS</span></span>

### <span data-ttu-id="88741-123">System.object</span><span class="sxs-lookup"><span data-stu-id="88741-123">System.String</span></span>

## <span data-ttu-id="88741-124">輸出</span><span class="sxs-lookup"><span data-stu-id="88741-124">OUTPUTS</span></span>

### <span data-ttu-id="88741-125">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="88741-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="88741-126">筆記</span><span class="sxs-lookup"><span data-stu-id="88741-126">NOTES</span></span>

## <span data-ttu-id="88741-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="88741-127">RELATED LINKS</span></span>

[<span data-ttu-id="88741-128">AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="88741-128">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="88741-129">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="88741-129">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


