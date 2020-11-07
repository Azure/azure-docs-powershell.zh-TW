---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801746"
---
# <span data-ttu-id="479e2-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="479e2-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="479e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="479e2-102">SYNOPSIS</span></span>
<span data-ttu-id="479e2-103">從虛擬機器移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="479e2-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="479e2-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="479e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="479e2-105">DESCRIPTION</span></span>
<span data-ttu-id="479e2-106">**AzureRmVMSqlServerExtension** Cmdlet 會從虛擬機器中移除 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="479e2-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="479e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="479e2-107">EXAMPLES</span></span>

### <span data-ttu-id="479e2-108">範例1：移除 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="479e2-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="479e2-109">這個命令會從名為 ContosoVM22 的虛擬機器中移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="479e2-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="479e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="479e2-110">PARAMETERS</span></span>

### <span data-ttu-id="479e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479e2-111">-DefaultProfile</span></span>
<span data-ttu-id="479e2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="479e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479e2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="479e2-113">-Name</span></span>
<span data-ttu-id="479e2-114">指定此 Cmdlet 移除之副檔名之 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="479e2-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="479e2-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="479e2-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479e2-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="479e2-117">-VMName</span></span>
<span data-ttu-id="479e2-118">指定此 Cmdlet 從中移除 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="479e2-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479e2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479e2-119">CommonParameters</span></span>
<span data-ttu-id="479e2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="479e2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479e2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="479e2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479e2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="479e2-122">INPUTS</span></span>

### <span data-ttu-id="479e2-123">所有</span><span class="sxs-lookup"><span data-stu-id="479e2-123">None</span></span>
<span data-ttu-id="479e2-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="479e2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="479e2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="479e2-125">OUTPUTS</span></span>

### <span data-ttu-id="479e2-126">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="479e2-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="479e2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="479e2-127">NOTES</span></span>

## <span data-ttu-id="479e2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="479e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="479e2-129">AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="479e2-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="479e2-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="479e2-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


