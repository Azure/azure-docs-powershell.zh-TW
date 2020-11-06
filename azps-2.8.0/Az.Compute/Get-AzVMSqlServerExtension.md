---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 9f0f9cfd25e630f0525a724fbec8f8b26ef872db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613362"
---
# <span data-ttu-id="547c6-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="547c6-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="547c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="547c6-102">SYNOPSIS</span></span>
<span data-ttu-id="547c6-103">取得虛擬機器上的 SQL Server 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="547c6-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="547c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="547c6-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="547c6-105">說明</span><span class="sxs-lookup"><span data-stu-id="547c6-105">DESCRIPTION</span></span>
<span data-ttu-id="547c6-106">**AzVMSqlServerExtension** Cmdlet 會取得 SQL Server 基礎結構的設定，成為虛擬機器上的服務 (IaaS) 代理程式。</span><span class="sxs-lookup"><span data-stu-id="547c6-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="547c6-107">示例</span><span class="sxs-lookup"><span data-stu-id="547c6-107">EXAMPLES</span></span>

### <span data-ttu-id="547c6-108">範例1：在虛擬機器上取得 SQL Server 延伸設定</span><span class="sxs-lookup"><span data-stu-id="547c6-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="547c6-109">這個命令會取得名為 ContosoVM07 的虛擬機器上的 SQL Server 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="547c6-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="547c6-110">範例2：使用管線取得設定</span><span class="sxs-lookup"><span data-stu-id="547c6-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="547c6-111">這個命令會透過使用 Get-AzVM Cmdlet，在服務 Service08 上取得名為 ContosoVM22 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="547c6-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="547c6-112">命令會使用管線運算子，將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="547c6-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="547c6-113">目前的命令會取得該虛擬機器上的 SQL Server IaaS 代理程式設定。</span><span class="sxs-lookup"><span data-stu-id="547c6-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="547c6-114">範例3：取得特定 SQL Server 版本的設定</span><span class="sxs-lookup"><span data-stu-id="547c6-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="547c6-115">這個命令會在名為 ContosoVM07 的虛擬機器上，取得 SQL Server 延伸版本1.0 的設定。</span><span class="sxs-lookup"><span data-stu-id="547c6-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="547c6-116">參數</span><span class="sxs-lookup"><span data-stu-id="547c6-116">PARAMETERS</span></span>

### <span data-ttu-id="547c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547c6-117">-DefaultProfile</span></span>
<span data-ttu-id="547c6-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="547c6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="547c6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="547c6-119">-Name</span></span>
<span data-ttu-id="547c6-120">指定副檔名的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="547c6-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="547c6-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="547c6-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="547c6-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="547c6-123">-VMName</span></span>
<span data-ttu-id="547c6-124">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="547c6-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547c6-125">CommonParameters</span></span>
<span data-ttu-id="547c6-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="547c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547c6-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="547c6-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547c6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="547c6-128">INPUTS</span></span>

### <span data-ttu-id="547c6-129">System.object</span><span class="sxs-lookup"><span data-stu-id="547c6-129">System.String</span></span>

## <span data-ttu-id="547c6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="547c6-130">OUTPUTS</span></span>

### <span data-ttu-id="547c6-131">VirtualMachineSqlServerExtensionCoNtext 的計算。</span><span class="sxs-lookup"><span data-stu-id="547c6-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="547c6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="547c6-132">NOTES</span></span>

## <span data-ttu-id="547c6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="547c6-133">RELATED LINKS</span></span>

[<span data-ttu-id="547c6-134">AzVM</span><span class="sxs-lookup"><span data-stu-id="547c6-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="547c6-135">移除-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="547c6-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="547c6-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="547c6-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


